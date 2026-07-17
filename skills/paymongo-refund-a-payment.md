---
name: Refund a payment
description: Find a completed Payment and issue a full or partial refund with a reason code, then confirm the refund status.
api: openapi/paymongo-openapi.yml
operations: [listPayments, retrievePayment, createRefund, retrieveRefund]
---

# Refund a payment (PayMongo)

Issue a full or partial refund against a completed Payment. All operationIds are
verified against `openapi/paymongo-openapi.yml`.

## Auth & conventions
- HTTP Basic with the secret key. Amounts in centavos. See
  `conventions/paymongo-conventions.yml`.

## Steps
1. **listPayments** (GET `/payments`) or **retrievePayment** (GET `/payments/{id}`)
   to locate the `pay_...` id and confirm `status: paid` and the `amount`
   available to refund.
2. **createRefund** — POST `/refunds` with `payment_id`, an `amount` in centavos
   (omit or set equal to the payment amount for a full refund), and a `reason`
   (`duplicate`, `fraudulent`, `requested_by_customer`, `others`). This reverses
   money — gate with human-in-the-loop for agents
   (`agentic-access/paymongo-agentic-access.yml`).
3. **retrieveRefund** — GET `/refunds/{id}` to confirm the refund reached a
   terminal status. Subscribe to the `refund.succeeded` webhook
   (`asyncapi/paymongo-webhooks.yml`) rather than polling.

## Errors
- A refund exceeding the remaining refundable amount is rejected — verify the
  net refundable amount before submitting. See
  `errors/paymongo-problem-types.yml`.
