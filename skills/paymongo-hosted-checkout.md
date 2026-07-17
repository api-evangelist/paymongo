---
name: Collect payment with a hosted Checkout Session
description: Create a PayMongo-hosted Checkout Session from your backend, redirect the customer to the checkout_url, and confirm or expire the session.
api: openapi/paymongo-openapi.yml
operations: [createCheckoutSession, retrieveCheckoutSession, expireCheckoutSession]
---

# Hosted Checkout (PayMongo)

Use PayMongo's hosted checkout when you don't want to build a payment UI. All
operationIds are verified against `openapi/paymongo-openapi.yml`.

## Auth & conventions
- HTTP Basic with the secret key (`sk_test_` / `sk_live_`). Amounts in centavos,
  currency `PHP`. See `conventions/paymongo-conventions.yml`.

## Steps
1. **createCheckoutSession** — POST `/checkout_sessions` with `line_items`
   (each `amount` in centavos), `payment_method_types`
   (e.g. `[card, gcash, grab_pay, paymaya]`), and `success_url` / `cancel_url`.
   Save `data.id` (`cs_...`) and `data.attributes.checkout_url`.
2. Redirect the customer to `checkout_url`. PayMongo hosts the payment page and
   handles method selection and 3DS.
3. **retrieveCheckoutSession** — GET `/checkout_sessions/{id}` after redirect to
   read `payment_intent`/`payments` and confirm the result. Prefer the
   `payment.paid` webhook (`asyncapi/paymongo-webhooks.yml`) over polling.
4. **expireCheckoutSession** — POST `/checkout_sessions/{id}/expire` to
   invalidate an unused session (e.g. cart abandoned or order cancelled).

## Notes
- In test mode use sandbox cards / e-wallet Authorize|Fail flows from
  `sandbox/paymongo-sandbox.yml`.
