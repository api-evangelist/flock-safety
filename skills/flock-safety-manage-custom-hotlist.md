---
name: Create a custom hotlist and add plate entries
description: Create an organization custom hotlist and batch-add license plates to alert on.
api: openapi/flock-safety-openapi-original.yml
operations:
  - POST /hotlists
  - GET /hotlists
  - POST /hotlists/{hotlistId}/entries/addBatch
  - GET /hotlists/{hotlistId}/entries
  - POST /hotlists/{hotlistId}/entries/deleteBatch
---

# Create a custom hotlist and add plate entries

Requires a token with the `custom-hotlists:read` / `custom-hotlists:write` scopes (the OpenAPI scheme
spells them `custom-holists:*` — a source typo; treat `custom-hotlists:*` as canonical).

## Steps

1. **Create the hotlist** — `POST /hotlists` with the hotlist name. Capture the returned `id`
   (`hotlistId`). (Or `GET /hotlists` to find an existing one.)
2. **Add plates in a batch** — `POST /hotlists/{hotlistId}/entries/addBatch` with the entries.
   Flock normalizes each plate (`O` → `0`), trims whitespace, and **ignores duplicates**, so
   re-submitting the same batch is safe (idempotent).
3. **Verify** — `GET /hotlists/{hotlistId}/entries` to page through stored entries.
4. **Remove plates** — `POST /hotlists/{hotlistId}/entries/deleteBatch` with the entry ids; ids that
   don't exist are ignored.

## Rules

- `400` on addBatch can indicate a duplicate plate or a malformed request.
- Custom hotlist matches drive LPR alert webhooks — pair this with the LPR alerts subscription skill.
- Respect data-stewardship: only list plates with a lawful, logged reason.
