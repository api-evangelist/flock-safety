# Flock Safety

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Flock Safety is a public safety technology company whose platform connects communities, businesses, and law enforcement through crime detection, investigation, and response tools built around license plate recognition (LPR) cameras, audio detection, video, and the FlockOS situational-awareness platform. Its v3 API Platform (api.flocksafety.com) lets approved customer organizations and third-party developers build "Flock Apps" that bring data in (register hardware as devices, ingest vehicle images for detection, push CAD events, alerts, and geolocation telemetry, manage custom hotlists) and connect Flock data out (retrieve devices, look up license plate reads, and subscribe to real-time LPR hotlist alert webhooks). The APIs use OAuth 2.0 with machine-level (client_credentials) and recommended user-level (authorization_code) flows, role-based access control, audit logging, and data-stewardship requirements.

**Areas:** Company · American Dynamism · Public Safety · Law Enforcement · License Plate Recognition · LPR · Physical Security · Surveillance · Computer Vision · Webhook · Geolocation · CAD

## Flock Safety on APIs.io

Everything profiled for Flock Safety is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/flock-safety/](https://apis.io/providers/flock-safety/)** — or go straight to one of the APIs or properties below.

### APIs (10)

- [Flock Safety Alerts API](https://apis.io/apis/flock-safety/flock-safety-alerts-api/) — The Alerts API from Flock Safety — 3 operation(s) for alerts.
- [Flock Safety CAD Events API](https://apis.io/apis/flock-safety/flock-safety-cad-events-api/) — The CAD Events API from Flock Safety — 7 operation(s) for cad events.
- [Flock Safety Custom Hotlists API](https://apis.io/apis/flock-safety/flock-safety-custom-hotlists-api/) — The Custom Hotlists API from Flock Safety — 5 operation(s) for custom hotlists.
- [Flock Safety Devices API](https://apis.io/apis/flock-safety/flock-safety-devices-api/) — The Devices API from Flock Safety — 3 operation(s) for devices.
- [Flock Safety LPR Hotlist Alert Subscriptions API](https://apis.io/apis/flock-safety/flock-safety-lpr-hotlist-alert-subscriptions-api/) — The LPR Hotlist Alert Subscriptions API from Flock Safety — 2 operation(s) for lpr hotlist alert subscriptions.
- [Flock Safety Plate Reads API](https://apis.io/apis/flock-safety/flock-safety-plate-reads-api/) — The Plate Reads API from Flock Safety — 2 operation(s) for plate reads.
- [Flock Safety Tracked Subject Types API](https://apis.io/apis/flock-safety/flock-safety-tracked-subject-types-api/) — The Tracked Subject Types API from Flock Safety — 2 operation(s) for tracked subject types.
- [Flock Safety Tracked Subjects API](https://apis.io/apis/flock-safety/flock-safety-tracked-subjects-api/) — The Tracked Subjects API from Flock Safety — 2 operation(s) for tracked subjects.
- [Flock Safety Vehicle Images API](https://apis.io/apis/flock-safety/flock-safety-vehicle-images-api/) — The Vehicle Images API from Flock Safety — 1 operation(s) for vehicle images.
- [Flock Safety O Auth2 API](https://apis.io/apis/flock-safety/flock-safety-oauth2-api/) — The OAuth2 API from Flock Safety — 1 operation(s) for oauth2.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Flock Safety LPR Hotlist Alerts Webhook](https://apis.io/asyncapis/flock-safety/flock-safety-lpr-alerts-asyncapi/)

#### Event channels (1)

Individual events and webhooks the provider emits.

- [lpr/hotlist-alert](https://apis.io/channels/flock-safety/lpr-hotlist-alert/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [flock-safety](https://apis.io/servers/flock-safety/flock-safety/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Flock Safety Agentic Access](https://apis.io/agentic-access/flock-safety/flock-safety-agentic-access/)

#### Collections (10)

Postman and Open Collection request collections.

- [Flock Safety API Platform (v3) Alerts API](https://apis.io/collections/flock-safety/open-flock-safety-alerts-api/)
- [Flock Safety API Platform (v3) Alerts CAD Events API](https://apis.io/collections/flock-safety/open-flock-safety-cad-events-api/)
- [Flock Safety API Platform (v3) Alerts Custom Hotlists API](https://apis.io/collections/flock-safety/open-flock-safety-custom-hotlists-api/)
- [Flock Safety API Platform (v3) Alerts Devices API](https://apis.io/collections/flock-safety/open-flock-safety-devices-api/)
- [Flock Safety API Platform (v3) Alerts LPR Hotlist Alert Subscriptions API](https://apis.io/collections/flock-safety/open-flock-safety-lpr-hotlist-alert-subscriptions-api/)
- [Flock Safety API Platform (v3) Alerts OAuth2 API](https://apis.io/collections/flock-safety/open-flock-safety-oauth2-api/)
- [Flock Safety API Platform (v3) Alerts Plate Reads API](https://apis.io/collections/flock-safety/open-flock-safety-plate-reads-api/)
- [Flock Safety API Platform (v3) Alerts Tracked Subject Types API](https://apis.io/collections/flock-safety/open-flock-safety-tracked-subject-types-api/)
- [Flock Safety API Platform (v3) Alerts Tracked Subjects API](https://apis.io/collections/flock-safety/open-flock-safety-tracked-subjects-api/)
- [Flock Safety API Platform (v3) Alerts Vehicle Images API](https://apis.io/collections/flock-safety/open-flock-safety-vehicle-images-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Flock Safety Api Platform Overlay](https://apis.io/overlays/flock-safety/flock-safety-api-platform-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Flock Safety Authentication](https://apis.io/security/flock-safety/flock-safety-authentication/)
- [Flock Safety Domain Security](https://apis.io/security/flock-safety/flock-safety-domain-security/)
- [Flock Safety Trust Center](https://apis.io/security/flock-safety/flock-safety-trust-center/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Flock Safety Scopes](https://apis.io/scopes/flock-safety/flock-safety-scopes/)

#### Rate limits (1)

Published request limits.

- [Flock Safety Rate Limits](https://apis.io/rate-limits/flock-safety/flock-safety-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://flocksafety.com)
- [Documentation](https://docs.flocksafety.com/developer-hub/docs/flock-developer-platform-overview)
- [Getting started](https://docs.flocksafety.com/developer-hub/docs/quickstart)
- [API reference](https://docs.flocksafety.com/developer-hub/reference/post_oauth-token)
- [Pricing](https://flocksafety.com/pricing)
- [Support](https://help.flocksafety.com/s/)
- [Changelog](https://docs.flocksafety.com/developer-hub/changelog)
- [Blog](https://flocksafety.com/blog)
- [Compliance](https://security.flocksafety.com/)
- [Terms of service](https://flocksafety.com/legal/terms-of-service)
- [Privacy policy](https://flocksafety.com/legal/privacy-notice)
- [GitHub](https://github.com/Flock-Safety)
- [Status](https://status.flocksafety.com/)

## API Evangelist rating

**Kin Score 51.5** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 57.8 |
| Contract governance | 4.5 |
| Operational transparency | 42.1 |
| Developer ergonomics | 44.6 |
| Access clarity | 47.4 |

**Agent readiness 36.6** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | documented (partial credit) |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 36.4** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/flock-safety/](https://apis.io/providers/flock-safety/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Flock Safety: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/flock-safety/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
