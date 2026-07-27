---
name: Upsert a CAD event and append a narrative
description: Create or update a computer-aided-dispatch event by externalId, add narrative, and close it.
api: openapi/flock-safety-openapi-original.yml
operations:
  - POST /cad/events
  - GET /cad/events
  - POST /cad/events/{externalId}/narrative
  - POST /cad/events/{externalId}/close
  - POST /cad/events/{externalId}/open
---

# Upsert a CAD event and append a narrative

Bring CAD (computer-aided dispatch) events into FlockOS. Events are keyed by a caller-supplied
`externalId`, which makes writes idempotent.

## Steps

1. **Create or update the event** — `POST /cad/events` with your `externalId` and event fields
   (caller info, involved persons/vehicles, dispatched units). If an event with that `externalId`
   already exists it is updated; otherwise it is created — so retries are safe.
2. **Append narrative** — `POST /cad/events/{externalId}/narrative` to add a timestamped narrative entry.
3. **Reconcile active events** — `POST /cad/events/active` upserts a set and closes any open events
   not included, keeping FlockOS in sync with your dispatch system.
4. **Close / reopen** — `POST /cad/events/{externalId}/close` (sets closedAt) and
   `POST /cad/events/{externalId}/open` (clears it).
5. **Read back** — `GET /cad/events` (most recent first) or `GET /cad/events/{externalId}`.

## Rules

- Reuse a stable `externalId` per source record so upserts stay idempotent (no duplicate events).
- Handle `404` (unknown externalId on close/narrative), `401`, and `429`.
