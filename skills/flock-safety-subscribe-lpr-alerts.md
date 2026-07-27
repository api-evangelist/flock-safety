---
name: Subscribe to real-time LPR hotlist alert webhooks
description: Register a webhook subscription to receive Flock LPR hotlist match alerts in real time.
api: openapi/flock-safety-openapi-original.yml
operations:
  - POST /integrations/lpr/alerts/subscriptions
  - GET /integrations/lpr/alerts/subscriptions
  - GET /integrations/lpr/alerts/subscriptions/{id}
  - PUT /integrations/lpr/alerts/subscriptions
  - DELETE /integrations/lpr/alerts/subscriptions/{id}
---

# Subscribe to real-time LPR hotlist alert webhooks

An LPR alert fires when a plate captured by a Flock camera (owned by, or shared within the customer's
First Responder Jurisdiction) matches an NCIC/CJIS or custom hotlist. Flock POSTs a JSON body to your
endpoint per match. See `asyncapi/flock-safety-lpr-alerts-asyncapi.yml` for the payload schema.

## Steps

1. **Stand up an HTTPS receiver** that accepts `POST` JSON and returns 2xx quickly.
2. **Create the subscription** — `POST /integrations/lpr/alerts/subscriptions` with your endpoint URL,
   the desired endpoint authentication (none | basic | apikey | oauth2 client_credentials), and the
   custom-hotlist audience filter (organization-only vs all custom hotlists including restricted).
3. **List / inspect** — `GET /integrations/lpr/alerts/subscriptions` and
   `GET /integrations/lpr/alerts/subscriptions/{id}`.
4. **Update or remove** — `PUT /integrations/lpr/alerts/subscriptions` to change config;
   `DELETE /integrations/lpr/alerts/subscriptions/{id}` to stop delivery.

## Rules

- Prefer OAuth2 endpoint auth: give Flock a token endpoint + client credentials; Flock sends
  `Authorization: Bearer <token>` on each webhook.
- Payload includes `objectId`, `eventTime`, device/network identity, a signed (expiring) `imageUrl`,
  `ocr` metadata, and `sources[]` (matched hotlists). Only CJIS and custom hotlist sources are supported.
- Deduplicate on `objectId`.
