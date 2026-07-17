---
name: Accept a card payment with a Payment Intent
description: Create a Payment Intent, create and attach a card Payment Method, then confirm the payment across PayMongo's Payment Intent workflow.
api: openapi/paymongo-openapi.yml
operations: [createPaymentIntent, createPaymentMethod, attachPaymentIntent, retrievePaymentIntent]
---

# Accept a card payment (PayMongo)

Operating instructions for accepting a card payment through PayMongo's Payment
Intent / Payment Method workflow. All operationIds are verified against
`openapi/paymongo-openapi.yml`.

## Auth & conventions
- HTTP Basic auth: the secret key `sk_test_...` / `sk_live_...` is the Basic-auth
  username, blank password. Public key `pk_test_...` may create Payment Methods
  client-side. Mode is chosen by the key prefix. See
  `conventions/paymongo-conventions.yml`.
- Amounts are integers in **centavos** (PHP 100.00 = `10000`). Currency `PHP`.
- Every request/response is wrapped in a `data.attributes` envelope.
- There is **no** Idempotency-Key header — rely on the intent lifecycle, do not
  blindly recreate intents on retry.

## Steps
1. **createPaymentIntent** — POST `/payment_intents` with `amount`, `currency: PHP`,
   and `payment_method_allowed: [card]` (add `capture_type: manual` for
   hold-then-capture). Save `data.id` (`pi_...`) and `data.attributes.client_key`.
2. **createPaymentMethod** — POST `/payment_methods` with `type: card` and card
   `details`. In test mode use a card from `sandbox/paymongo-sandbox.yml`
   (e.g. `4343434343434345`). Save `data.id` (`pm_...`).
3. **attachPaymentIntent** — POST `/payment_intents/{id}/attach` with the
   `payment_method` id and a `return_url`. This authorizes/moves money — gate it
   with human-in-the-loop when run by an agent (see
   `agentic-access/paymongo-agentic-access.yml`).
4. Handle `next_action`: if `data.attributes.status` is `awaiting_next_action`,
   redirect the customer to `next_action.redirect.url` for 3DS, then return to
   `return_url`.
5. **retrievePaymentIntent** — GET `/payment_intents/{id}` to confirm the final
   status (`succeeded`, or back to `awaiting_payment_method` on failure). Prefer
   the `payment.paid` / `payment.failed` webhook over polling
   (`asyncapi/paymongo-webhooks.yml`).

## Errors
- Card declines surface as a `sub_code` on the failed payment — see
  `errors/paymongo-decline-codes.yml`. Never expose the masked fraud/lost/stolen
  sub codes to buyers; present them as a generic decline.
