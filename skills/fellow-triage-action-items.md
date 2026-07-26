---
name: Triage and complete action items
description: List a user's Fellow action items with scope/status filters, inspect one, then mark it complete or archive it as won't-do.
api: Fellow Developer API
base_url: https://{subdomain}.fellow.app/api/v1
operations:
  - apps_developer_api_api_get_action_items
  - apps_developer_api_api_get_action_item_by_id
  - apps_developer_api_api_mark_action_item_complete
  - apps_developer_api_api_archive_action_item
---

# Triage and complete action items

Automate follow-through on meeting action items from an external tool.

## Auth
`X-API-KEY: <your key>` on every request (see the transcripts skill for key setup).

## Steps
1. **List** — `apps_developer_api_api_get_action_items` with cursor pagination and an
   optional `scope` filter:
   - default: all action items the user can access
   - `assigned_to_me`: only items assigned to the caller
   - `assigned_to_others`: editable items assigned to teammates
   With a privileged (super-admin) key, listing covers the whole account.
2. **Inspect** — `apps_developer_api_api_get_action_item_by_id` (`GET /action-items/{id}`)
   for text, assignees, `status` (Incomplete / Done / Archived), and `due_date`.
3. **Complete or reopen** — `apps_developer_api_api_mark_action_item_complete` to
   toggle completion.
4. **Archive** — `apps_developer_api_api_archive_action_item` to mark an item as won't-do.

## Rules
- `completion_type` is `any` (one assignee) or `all` (every assignee must complete).
- Respect 3 req/s + 10,000 req/day; retry on 429.
- To react in real time instead of polling, subscribe to `action_item.assigned` /
  `action_item.completed` webhooks (see the webhooks skill).
