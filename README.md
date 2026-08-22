# PayMongo (paymongo)

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

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/paymongo/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/paymongo/refs/heads/main/apis.yml)

## Tags

- Payments
- FinTech
- Philippines
- Southeast Asia
- GCash
- E-Wallet
- Card Payments

## Timestamps

- **Created:** 2026-07-17
- **Modified:** 2026-07-17

## APIs

### PayMongo Payment Intents API

Core payment-acceptance workflow. Create a Payment Intent, attach a Payment Method, and confirm the payment across cards, GCash, Maya, GrabPay, QR Ph, BillEase, and direct online banking, with manual or automatic capture.

- **Human URL:** [https://docs.paymongo.com/reference/the-payment-intent-object](https://docs.paymongo.com/reference/the-payment-intent-object)
- **Base URL:** `https://api.paymongo.com/v1`

#### Tags

- Payment Intents
- Payments
- Checkout

#### Properties

- [Documentation](https://docs.paymongo.com/docs/payment-acceptance-introduction)
- [API Reference](https://docs.paymongo.com/reference/create-a-paymentintent)
- [OpenAPI](openapi/paymongo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/paymongo.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### PayMongo Payment Methods API

Creates and retrieves Payment Method resources describing how the customer pays (card, gcash, grab_pay, paymaya, billease, dob, qrph). May be created with the public or secret API key.

- **Human URL:** [https://docs.paymongo.com/reference/the-payment-method-object](https://docs.paymongo.com/reference/the-payment-method-object)
- **Base URL:** `https://api.paymongo.com/v1`

#### Tags

- Payment Methods
- Cards
- E-Wallet

#### Properties

- [API Reference](https://docs.paymongo.com/reference/create-a-paymentmethod)
- [OpenAPI](openapi/paymongo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/paymongo.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### PayMongo Payments API

Lists and retrieves completed Payment resources with amount, fee, net_amount, and status for reconciliation.

- **Human URL:** [https://docs.paymongo.com/reference/list-all-payments](https://docs.paymongo.com/reference/list-all-payments)
- **Base URL:** `https://api.paymongo.com/v1`

#### Tags

- Payments
- Transactions

#### Properties

- [API Reference](https://docs.paymongo.com/reference/list-all-payments)
- [OpenAPI](openapi/paymongo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/paymongo.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### PayMongo Sources API

Legacy Sources workflow for GCash and GrabPay redirect payments. PayMongo recommends migrating to the Payment Intent workflow; documented here for existing integrations.

- **Human URL:** [https://docs.paymongo.com/docs/older-workflows](https://docs.paymongo.com/docs/older-workflows)
- **Base URL:** `https://api.paymongo.com/v1`

#### Tags

- Sources
- GCash
- GrabPay
- Legacy

#### Properties

- [Documentation](https://docs.paymongo.com/docs/older-workflows)
- [OpenAPI](openapi/paymongo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/paymongo.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### PayMongo Checkout Sessions API

Creates a PayMongo-hosted checkout page from your backend, returning a checkout_url to redirect the customer to. Sessions can be retrieved and expired.

- **Human URL:** [https://docs.paymongo.com/reference/checkout-session-resource](https://docs.paymongo.com/reference/checkout-session-resource)
- **Base URL:** `https://api.paymongo.com/v1`

#### Tags

- Hosted Checkout
- Checkout

#### Properties

- [Documentation](https://docs.paymongo.com/docs/payment-channels-hosted-checkout)
- [API Reference](https://docs.paymongo.com/reference/create_checkout_sessions)
- [OpenAPI](openapi/paymongo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/paymongo.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### PayMongo Payment Links API

Creates, lists, updates, and refunds shareable Payment Links that collect a fixed or open amount without building a checkout UI.

- **Human URL:** [https://docs.paymongo.com/reference/payment-links](https://docs.paymongo.com/reference/payment-links)
- **Base URL:** `https://api.paymongo.com/v1`

#### Tags

- Payment Links
- No Code

#### Properties

- [Documentation](https://docs.paymongo.com/docs/payment-channels-payment-links)
- [API Reference](https://docs.paymongo.com/reference/post_v1-payment-links)
- [OpenAPI](openapi/paymongo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/paymongo.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### PayMongo Customers API

Manages Customer objects and their vaulted payment methods for repeat purchases and card-on-file flows.

- **Human URL:** [https://docs.paymongo.com/reference/retrieve-customer](https://docs.paymongo.com/reference/retrieve-customer)
- **Base URL:** `https://api.paymongo.com/v1`

#### Tags

- Customers
- Vaulting

#### Properties

- [Documentation](https://docs.paymongo.com/docs/payment-acceptance-card-vaulting)
- [API Reference](https://docs.paymongo.com/reference/retrieve-customer)
- [OpenAPI](openapi/paymongo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/paymongo.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### PayMongo Refunds API

Issues full or partial refunds against a Payment, with reason codes (duplicate, fraudulent, requested_by_customer, others).

- **Human URL:** [https://docs.paymongo.com/docs/payment-acceptance-refunds](https://docs.paymongo.com/docs/payment-acceptance-refunds)
- **Base URL:** `https://api.paymongo.com/v1`

#### Tags

- Refunds
- Disputes

#### Properties

- [Documentation](https://docs.paymongo.com/docs/payment-acceptance-refunds)
- [OpenAPI](openapi/paymongo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/paymongo.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### PayMongo QR Ph API

Generates dynamic (API-driven) and static (in-store) QR Ph codes - the Philippine national QR standard - and confirms payment via webhook or polling.

- **Human URL:** [https://docs.paymongo.com/docs/payment-acceptance-qr-ph-api](https://docs.paymongo.com/docs/payment-acceptance-qr-ph-api)
- **Base URL:** `https://api.paymongo.com/v1`

#### Tags

- QR Ph
- QR Code
- In Store

#### Properties

- [Documentation](https://docs.paymongo.com/docs/payment-acceptance-qr-ph)
- [API Reference](https://docs.paymongo.com/reference/generate-mpm-qr)
- [OpenAPI](openapi/paymongo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/paymongo.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### PayMongo Webhooks API

Registers, lists, enables, and disables webhook endpoints. Deliveries are signed HTTP POST callbacks (Paymongo-Signature header) for events such as payment.paid, payment.failed, and source.chargeable - not a WebSocket stream.

- **Human URL:** [https://docs.paymongo.com/docs/developer-tools-webhooks](https://docs.paymongo.com/docs/developer-tools-webhooks)
- **Base URL:** `https://api.paymongo.com/v1`

#### Tags

- Webhooks
- Events

#### Properties

- [Documentation](https://docs.paymongo.com/docs/developer-tools-webhooks)
- [API Reference](https://docs.paymongo.com/reference/create-a-webhook)
- [OpenAPI](openapi/paymongo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/paymongo.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)

### PayMongo Subscriptions & Plans API

Creates Plans and Subscriptions for recurring billing, including invoices, on-demand payments, and test-cycle triggers.

- **Human URL:** [https://docs.paymongo.com/reference/subscription-resource](https://docs.paymongo.com/reference/subscription-resource)
- **Base URL:** `https://api.paymongo.com/v1`

#### Tags

- Subscriptions
- Recurring
- Billing

#### Properties

- [Documentation](https://docs.paymongo.com/docs/payment-acceptance-subscriptions)
- [API Reference](https://docs.paymongo.com/reference/create-a-subscription)
- [OpenAPI](openapi/paymongo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### PayMongo Money Movement API

Wallets, Transfers, Batch Transfers, and Payouts to move funds out to banks and e-wallets via InstaPay and PESONet, with reconciliation endpoints.

- **Human URL:** [https://docs.paymongo.com/docs/money-movement-introduction](https://docs.paymongo.com/docs/money-movement-introduction)
- **Base URL:** `https://api.paymongo.com/v1`

#### Tags

- Wallets
- Transfers
- Payouts
- Disbursements

#### Properties

- [Documentation](https://docs.paymongo.com/docs/money-movement-moving-money-with-api)
- [API Reference](https://docs.paymongo.com/reference/transfer-resource)
- [OpenAPI](openapi/paymongo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### PayMongo Forex API

Locks in a price for converting between the Philippine Peso and supported foreign currencies via Rates and Quotes, settled across the platform.

- **Human URL:** [https://docs.paymongo.com/docs/money-movement-forex](https://docs.paymongo.com/docs/money-movement-forex)
- **Base URL:** `https://api.paymongo.com/v1`

#### Tags

- Forex
- Currency
- Quotes

#### Properties

- [Documentation](https://docs.paymongo.com/docs/money-movement-forex)
- [API Reference](https://docs.paymongo.com/reference/quote-resource)
- [OpenAPI](openapi/paymongo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

### PayMongo Fraud Detection API

PayMongo Protect - Reviews, Rules, Rule Attributes, and Scores for per-transaction risk scoring and manual review workflows.

- **Human URL:** [https://docs.paymongo.com/reference/fraud-detection-overview](https://docs.paymongo.com/reference/fraud-detection-overview)
- **Base URL:** `https://api.paymongo.com/v1`

#### Tags

- Fraud
- Risk
- Protect

#### Properties

- [API Reference](https://docs.paymongo.com/reference/fraud-detection-overview)
- [OpenAPI](openapi/paymongo-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)

## Common Properties

- [GitHub Organization](https://github.com/paymongo)
- [LinkedIn](https://www.linkedin.com/company/paymongo)
- [Website](https://www.paymongo.com/)
- [Documentation](https://docs.paymongo.com/)
- [Plans](plans/paymongo-plans-pricing.yml)
- [Rate Limits](rate-limits/paymongo-rate-limits.yml)
- [Fin Ops](finops/paymongo-finops.yml)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
