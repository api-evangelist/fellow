---
name: Pull recent meeting recordings and transcripts
description: Authenticate to the Fellow Developer API, confirm the workspace, then page through recent recordings and fetch a recording's transcript and metadata.
api: Fellow Developer API
base_url: https://{subdomain}.fellow.app/api/v1
operations:
  - apps_developer_api_api_get_authenticated_user
  - apps_developer_api_api_get_recordings
  - apps_developer_api_api_get_recording_by_id
---

# Pull recent meeting recordings and transcripts

Use this to feed meeting transcripts/notes into an LLM, a dashboard, or a compliance archive.

## Prerequisites
- A paid Fellow workspace with the Developer API enabled (admin: Security settings).
- A personal API key (User Settings -> Developer API). Keep it secret; it is shown once.

## Auth
Send the key on every request in the `X-API-KEY` header. Replace `{subdomain}` with your workspace subdomain.

```
X-API-KEY: <your key>
```

## Steps
1. **Confirm the caller** — call `apps_developer_api_api_get_authenticated_user`
   (`GET /me`) to verify the key and read the user + workspace.
2. **List recordings** — call `apps_developer_api_api_get_recordings`
   (`POST /recordings`) with a `pagination` body: `{ "pagination": { "cursor": null, "page_size": 20 } }`.
   Cursor-based: pass the returned `page_info.cursor` on the next call; stop when it is `null`.
3. **Fetch one recording** — call `apps_developer_api_api_get_recording_by_id`
   (`GET /recordings/{id}`) to get the transcript, notes, and metadata.

## Rules
- Rate limits: 3 req/s and 10,000 req/day per key — back off on HTTP 429 (`rate_limited`).
- You only ever see resources the key owner can access in Fellow (attendee / shared / channel).
- Errors are `{ "message": ..., "errors": [...] }` JSON; 401 = bad key, 403 = no access.
