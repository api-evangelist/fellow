---
name: Subscribe to real-time meeting webhooks
description: Register a Fellow webhook (passing URL verification), verify svix signatures on delivery, and manage the subscription lifecycle.
api: Fellow Developer API
base_url: https://{subdomain}.fellow.app/api/v1
operations:
  - apps_developer_api_api_create_webhook
  - apps_developer_api_api_list_webhooks
  - apps_developer_api_api_get_webhook_by_id
  - apps_developer_api_api_update_webhook
  - apps_developer_api_api_delete_webhook
---

# Subscribe to real-time meeting webhooks

React instantly to Fellow events instead of polling.

## Prerequisites
- Webhooks enabled for the workspace; a Developer API key.
- A public HTTPS endpoint with a valid (non-self-signed) certificate.

## URL verification (happens first)
On create/URL-update Fellow POSTs `{ "type": "url_verification", "challenge": "<str>" }`.
Respond `200` with the raw `challenge` string as plain text within 10 seconds.

## Steps
1. **Create** — `apps_developer_api_api_create_webhook` (`POST /webhooks`) with
   `{ url, enabled_events, description, status: "active" }`. Valid events:
   `ai_note.generated`, `ai_note.shared_to_channel`, `action_item.assigned`,
   `action_item.completed`. **Save the returned `secret` (`whsec_...`) — shown once.**
2. **Verify each delivery** — every event carries `svix-id`, `svix-timestamp`,
   `svix-signature`. Compute HMAC-SHA256 over `{svix-id}.{svix-timestamp}.{raw-body}`
   with the base64-decoded secret; compare against the `v1,<b64>` signature using a
   constant-time compare. Reject timestamps older than 5 minutes.
3. **Acknowledge** — return a 2xx within 15 seconds; process async. Non-2xx triggers
   retries (8 attempts over ~27h); 5 days of failure auto-disables the endpoint (`failed`).
4. **Manage** — `apps_developer_api_api_list_webhooks` /
   `apps_developer_api_api_get_webhook_by_id` /
   `apps_developer_api_api_update_webhook` (reactivate a `failed` one by setting
   `status: active`) / `apps_developer_api_api_delete_webhook`.

## Rules
- Use the **raw** request body for signature checks — parsing JSON first breaks them.
- URLs must be public HTTPS (no private/loopback/link-local IPs, no embedded creds).
- De-dupe retried deliveries by `svix-id`.
