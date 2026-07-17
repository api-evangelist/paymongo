---
name: Register and verify webhooks
description: Register a webhook endpoint, verify delivery signatures, and enable or disable endpoints to receive PayMongo payment events reliably.
api: openapi/paymongo-openapi.yml
operations: [createWebhook, listWebhooks, retrieveWebhook, enableWebhook, disableWebhook]
---

# Handle webhooks (PayMongo)

Receive PayMongo payment events reliably. All operationIds are verified against
`openapi/paymongo-openapi.yml`; the event catalog is in
`asyncapi/paymongo-webhooks.yml`.

## Auth & conventions
- HTTP Basic with the secret key. Deliveries are signed HTTP POST callbacks
  (not a stream). See `conventions/paymongo-conventions.yml`.

## Steps
1. **createWebhook** — POST `/webhooks` with your HTTPS `url` and the `events`
   you want (e.g. `payment.paid`, `payment.failed`, `refund.succeeded`). Save the
   returned `secret_key` — it is shown once and is required to verify signatures.
2. **listWebhooks** (GET `/webhooks`) / **retrieveWebhook** (GET `/webhooks/{id}`)
   to audit registered endpoints.
3. On each delivery, verify the **`Paymongo-Signature`** header: compute an HMAC
   over the raw request body using the endpoint's signing secret and compare.
   Reject on mismatch. Respond `200` quickly and process asynchronously.
4. Dedupe on the event `data.id` (`evt_...`) — deliveries may repeat.
5. **disableWebhook** (POST `/webhooks/{id}/disable`) / **enableWebhook**
   (POST `/webhooks/{id}/enable`) to pause or resume an endpoint (e.g. during
   maintenance or after repeated failures).

## Notes
- Use test-mode keys and the sandbox flows in `sandbox/paymongo-sandbox.yml` to
  trigger events before going live.
