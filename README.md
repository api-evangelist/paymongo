# PayMongo (paymongo)

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
