---
name: Look up license plate reads
description: Perform an on-demand license plate read lookup and page through the results.
api: openapi/flock-safety-openapi-original.yml
operations:
  - POST /reads/lookup
  - GET /reads/lookup/page/{pageId}
---

# Look up license plate reads

Requires a token with the `plate-reads:lookup` scope (the `FlockOAuth` client-credentials scheme).
This is a sensitive, audited operation — supply a lawful query reason.

## Steps

1. **Start a lookup** — `POST /reads/lookup` (base `https://api.flocksafety.com/api/v3`) with the full
   license plate characters and any filters (area/radius, time, confidence) documented in the request
   body. The response returns the first page plus a `pageId` for continuation.
2. **Page through results** — `GET /reads/lookup/page/{pageId}` to retrieve subsequent result pages.

## Rules

- Fetch on demand for a specific investigation; do **not** bulk-scrape (data-stewardship requirement).
- Every lookup should carry an auditable reason; user-level OAuth attributes the action to the user.
- Handle `401` (refresh token + retry), `403` (missing scope/access), and `429` (rate limit — back off).
