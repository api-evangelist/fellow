# Fellow

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

Fellow is an AI meeting assistant and meeting-management platform that records, transcribes, and summarizes meetings, then captures structured notes, action items, and decisions across a team's calendar. Fellow's Developer API opens that meeting data through a REST interface: authenticated workspace users generate personal API keys and retrieve recordings, transcripts, notes, and action items, upload recordings, and manage webhook subscriptions for real-time events. Fellow also publishes a hosted, OAuth-secured Model Context Protocol (MCP) server so AI assistants like Claude and ChatGPT can query meeting context in natural language. Backed by Craft Ventures and Felicis. The API requires a paid workspace plan and is governed by workspace admins under Security settings, with a 90-day audit log, SOC 2 Type II, HIPAA BAA availability, and GDPR/CCPA support.

**Areas:** Company · Software-as-a-Service · Meetings · Artificial Intelligence · Meeting Notes · Transcription · Productivity · Action Items · Webhook · MCP

## Fellow on APIs.io

Everything profiled for Fellow is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/fellow/](https://apis.io/providers/fellow/)** — or go straight to one of the APIs or properties below.

### APIs (5)

- [Fellow Action Items API](https://apis.io/apis/fellow/fellow-action-items-api/) — Access and manage action items from meetings. Retrieve, list, complete, or archive action items with optional filters and pagination.
- [Fellow Notes API](https://apis.io/apis/fellow/fellow-notes-api/) — Access and manage meeting notes and their agendas. Retrieve individual notes, list notes with filters and pagination, delete notes (privileged access…
- [Fellow Recordings API](https://apis.io/apis/fellow/fellow-recordings-api/) — Access and manage meeting recordings. Retrieve individual recordings, list recordings with filters and pagination, or delete recordings (privileged access…
- [Fellow Users API](https://apis.io/apis/fellow/fellow-users-api/) — Retrieve information about the currently authenticated user and their workspace.
- [Fellow Webhooks API](https://apis.io/apis/fellow/fellow-webhooks-api/) — Create and manage webhook endpoints to receive real-time notifications when events occur in your Fellow workspace.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Fellow Webhooks](https://apis.io/asyncapis/fellow/fellow-webhooks-asyncapi/)

#### Event channels (1)

Individual events and webhooks the provider emits.

- [/](https://apis.io/channels/fellow/webhook/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [fellow](https://apis.io/servers/fellow/fellow/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Fellow Agentic Access](https://apis.io/agentic-access/fellow/fellow-agentic-access/)

#### JSON Schema (6)

The data models the API reads and writes.

- [CreateWebhookRequest](https://apis.io/schemas/fellow/fellow-create-webhook-request/)
- [FindReplaceNoteAgendaRequest](https://apis.io/schemas/fellow/fellow-find-replace-note-agenda-request/)
- [GetActionItemsRequest](https://apis.io/schemas/fellow/fellow-get-action-items-request/)
- [RecordingUploadRequest](https://apis.io/schemas/fellow/fellow-recording-upload-request/)
- [UpdateWebhookRequest](https://apis.io/schemas/fellow/fellow-update-webhook-request/)
- [WriteNoteAgendaRequest](https://apis.io/schemas/fellow/fellow-write-note-agenda-request/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Fellow Context](https://apis.io/jsonld/fellow/fellow-context/)

#### Governance rules (1)

Spectral rulesets for the provider's contracts.

- [Fellow API Rules](https://apis.io/rules/fellow/fellow-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Fellow Authentication](https://apis.io/security/fellow/fellow-authentication/)
- [Fellow Domain Security](https://apis.io/security/fellow/fellow-domain-security/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Fellow Scopes](https://apis.io/scopes/fellow/fellow-scopes/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Fellow Plans Pricing](https://apis.io/plans/fellow/fellow-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Fellow Rate Limits](https://apis.io/rate-limits/fellow/fellow-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://fellow.ai)
- [Documentation](https://developers.fellow.ai/)
- [Getting started](https://developers.fellow.ai/reference/authentication-1)
- [API reference](https://developers.fellow.ai/reference/introduction)
- [Pricing](https://fellow.ai/pricing)
- [Sign up](https://fellow.app/auth/login/)
- [Support](https://help.fellow.ai/)
- [Blog](https://fellow.ai/blog)
- [Security](https://fellow.ai/security)
- [Compliance](https://help.fellow.ai/en/articles/4302231-security-and-compliance)
- [Trust centre](https://trust.fellow.ai/)
- [Terms of service](https://fellow.ai/terms-of-use)
- [Privacy policy](https://fellow.ai/privacy-policy)
- [GitHub](https://github.com/fellowapp)
- [Status](https://status.fellow.ai/)

## API Evangelist rating

**Kin Score 67.2** — exemplar · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 78.3 |
| Contract quality | 67.3 |
| Contract governance | 35.6 |
| Operational transparency | 73.7 |
| Developer ergonomics | 47.0 |
| Access clarity | 84.2 |

**Agent readiness 50.5** — agent-ready (gated down from agent-native)

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | verified |
| Auth Clarity | served (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | derived (partial credit) |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | served (partial credit) |
| Protected Resource Metadata | verified |
| Dynamic Client Registration | yes |
| Agentic Commerce | — |
| Pagination Ratio | na |
| Operation Distinctiveness | distinct |

**Regulatory alignment 36.4** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/fellow/](https://apis.io/providers/fellow/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Fellow: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/fellow/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
