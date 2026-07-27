---
name: Get a Flock Safety API access token
description: Exchange org-provisioned client credentials for a Bearer token to call the Flock Safety v3 API.
api: openapi/flock-safety-openapi-original.yml
operations:
  - POST /oauth/token
---

# Get a Flock Safety API access token

Flock Safety v3 APIs use OAuth 2.0. Credentials (`client_id` / `client_secret`) are provisioned
privately per customer organization by a Flock Safety representative — there is no self-service signup.

## Steps

1. **Request a machine (org-level) token** — `POST https://api.flocksafety.com/oauth/token`
   with `Content-Type: application/x-www-form-urlencoded` and body fields:
   - `grant_type=client_credentials`
   - `client_id=<your_client_id>`
   - `client_secret=<your_client_secret>`
   - `audience=com.flocksafety.integrations` (use `com.flocksafety.integrations.dev` against the
     `https://dev-api.flocksafety.com` sandbox, when Flock has enabled one for you)
2. **Read the response** — `{ "access_token", "token_type": "Bearer", "expires_in": 86400 }`.
   Machine tokens live 24 hours and have **no** refresh token.
3. **Call the API** — send `Authorization: Bearer {access_token}` on every request to
   `https://api.flocksafety.com/api/v3/...`.
4. **Refresh on expiry** — when a call returns `401`, request a new token and retry (see rules below).

For sensitive endpoints Flock recommends **user-level OAuth** (`authorization_code`), whose access
tokens live 30 minutes and refresh via a 12-hour refresh token (token rotation).

## Rules

- The token is a JWT and is case-sensitive.
- Handle `401 Unauthorized` by fetching a fresh token and retrying the request.
- `403` on `/oauth/token` means an invalid or missing `audience`.
- Allowlist trusted IP addresses; store credentials and tokens securely.
