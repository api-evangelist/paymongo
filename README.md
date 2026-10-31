# PayMongo

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

PayMongo is a Philippine payments platform that lets businesses accept online payments via cards, GCash, Maya (PayMaya), GrabPay, ShopeePay, QR Ph, BillEase buy-now-pay-later, and direct online banking. Its REST API is built around the Payment Intent / Payment Method workflow with hosted Checkout Sessions, Payment Links, Customers, Refunds, Subscriptions, and signed Webhooks. Amounts are integers in centavos and PHP is the settlement currency; PayMongo is a PCI DSS Level 1 Service Provider.

**Areas:** Payments · Fintech · Philippines · Southeast Asia · GCash · Digital Wallet · Card Payments

## PayMongo on APIs.io

Everything profiled for PayMongo is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/paymongo/](https://apis.io/providers/paymongo/)** — or go straight to one of the APIs or properties below.

### APIs (10)

- [PayMongo Checkout Sessions API](https://apis.io/apis/paymongo/paymongo-checkout-sessions-api/) — The Checkout Sessions API from PayMongo — 3 operation(s) for checkout sessions.
- [PayMongo Customers API](https://apis.io/apis/paymongo/paymongo-customers-api/) — The Customers API from PayMongo — 2 operation(s) for customers.
- [PayMongo Payment Intents API](https://apis.io/apis/paymongo/paymongo-payment-intents-api/) — The Payment Intents API from PayMongo — 3 operation(s) for payment intents.
- [PayMongo Payment Links API](https://apis.io/apis/paymongo/paymongo-payment-links-api/) — The Payment Links API from PayMongo — 2 operation(s) for payment links.
- [PayMongo Payment Methods API](https://apis.io/apis/paymongo/paymongo-payment-methods-api/) — The Payment Methods API from PayMongo — 2 operation(s) for payment methods.
- [PayMongo Payments API](https://apis.io/apis/paymongo/paymongo-payments-api/) — The Payments API from PayMongo — 2 operation(s) for payments.
- [PayMongo QR Ph API](https://apis.io/apis/paymongo/paymongo-qr-ph-api/) — The QR Ph API from PayMongo — 1 operation(s) for qr ph.
- [PayMongo Refunds API](https://apis.io/apis/paymongo/paymongo-refunds-api/) — The Refunds API from PayMongo — 2 operation(s) for refunds.
- [PayMongo Sources API](https://apis.io/apis/paymongo/paymongo-sources-api/) — The Sources API from PayMongo — 2 operation(s) for sources.
- [PayMongo Webhooks API](https://apis.io/apis/paymongo/paymongo-webhooks-api/) — The Webhooks API from PayMongo — 4 operation(s) for webhooks.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Paymongo Webhooks](https://apis.io/asyncapis/paymongo/paymongo-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [paymongo](https://apis.io/servers/paymongo/paymongo/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Paymongo Agentic Access](https://apis.io/agentic-access/paymongo/paymongo-agentic-access/)

#### Collections (20)

Postman and Open Collection request collections.

- [PayMongo Checkout Sessions API](https://apis.io/collections/paymongo/open-paymongo-checkout-sessions-api/)
- [PayMongo Checkout Sessions Customers API](https://apis.io/collections/paymongo/open-paymongo-customers-api/)
- [PayMongo Checkout Sessions Payment Intents API](https://apis.io/collections/paymongo/open-paymongo-payment-intents-api/)
- [PayMongo Checkout Sessions Payment Links API](https://apis.io/collections/paymongo/open-paymongo-payment-links-api/)
- [PayMongo Checkout Sessions Payment Methods API](https://apis.io/collections/paymongo/open-paymongo-payment-methods-api/)
- [PayMongo Checkout Sessions Payments API](https://apis.io/collections/paymongo/open-paymongo-payments-api/)
- [PayMongo Checkout Sessions QR Ph API](https://apis.io/collections/paymongo/open-paymongo-qr-ph-api/)
- [PayMongo Checkout Sessions Refunds API](https://apis.io/collections/paymongo/open-paymongo-refunds-api/)
- [PayMongo Checkout Sessions Sources API](https://apis.io/collections/paymongo/open-paymongo-sources-api/)
- [PayMongo Checkout Sessions Webhooks API](https://apis.io/collections/paymongo/open-paymongo-webhooks-api/)
- [PayMongo Checkout Sessions API](https://apis.io/collections/paymongo/postman-paymongo-checkout-sessions-api/)
- [PayMongo Checkout Sessions Customers API](https://apis.io/collections/paymongo/postman-paymongo-customers-api/)
- [PayMongo Checkout Sessions Payment Intents API](https://apis.io/collections/paymongo/postman-paymongo-payment-intents-api/)
- [PayMongo Checkout Sessions Payment Links API](https://apis.io/collections/paymongo/postman-paymongo-payment-links-api/)
- [PayMongo Checkout Sessions Payment Methods API](https://apis.io/collections/paymongo/postman-paymongo-payment-methods-api/)
- [PayMongo Checkout Sessions Payments API](https://apis.io/collections/paymongo/postman-paymongo-payments-api/)
- [PayMongo Checkout Sessions QR Ph API](https://apis.io/collections/paymongo/postman-paymongo-qr-ph-api/)
- [PayMongo Checkout Sessions Refunds API](https://apis.io/collections/paymongo/postman-paymongo-refunds-api/)
- [PayMongo Checkout Sessions Sources API](https://apis.io/collections/paymongo/postman-paymongo-sources-api/)
- [PayMongo Checkout Sessions Webhooks API](https://apis.io/collections/paymongo/postman-paymongo-webhooks-api/)

#### Overlays (1)

OpenAPI overlays, including conversational phrasing for each operation.

- [Paymongo Openapi Overlay](https://apis.io/overlays/paymongo/paymongo-openapi-overlay/)

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Paymongo Authentication](https://apis.io/security/paymongo/paymongo-authentication/)
- [Paymongo Domain Security](https://apis.io/security/paymongo/paymongo-domain-security/)
- [Paymongo Trust Center](https://apis.io/security/paymongo/paymongo-trust-center/)
- [Paymongo Vulnerability Disclosure](https://apis.io/security/paymongo/paymongo-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Paymongo Plans Pricing](https://apis.io/plans/paymongo/paymongo-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Paymongo Rate Limits](https://apis.io/rate-limits/paymongo/paymongo-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Paymongo Finops](https://apis.io/finops/paymongo/paymongo-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.paymongo.com/)
- [Documentation](https://docs.paymongo.com/)
- [Getting started](https://docs.paymongo.com/docs/payment-acceptance-quick-start)
- [API reference](https://docs.paymongo.com/reference)
- [Pricing](https://www.paymongo.com/pricing)
- [Sign up](https://dashboard.paymongo.com/signup)
- [Blog](https://www.paymongo.com/blog)
- [Security](https://docs.paymongo.com/docs/keeping-payments-secure)
- [Compliance](https://www.paymongo.com/secure)
- [Terms of service](https://www.paymongo.com/terms)
- [Privacy policy](https://www.paymongo.com/privacy)
- [GitHub](https://github.com/paymongo)
- [Status](https://status.paymongo.com)

## API Evangelist rating

**Kin Score 57.7** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 55.0 |
| Contract governance | 18.2 |
| Operational transparency | 48.7 |
| Developer ergonomics | 63.7 |
| Access clarity | 61.8 |

**Agent readiness 31.6** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | documented (partial credit) |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
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
| Pagination Ratio | paginated |
| Operation Distinctiveness | distinct |

**Regulatory alignment 44.6** — Payments

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/paymongo/](https://apis.io/providers/paymongo/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for PayMongo: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/paymongo/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
