---
name: Send an SMS over the KPN network and handle the delivery report
description: Authenticate against the KPN API Store, send a single or bulk SMS through the KPN SMS API, and correctly verify and interpret the signed delivery-report webhook.
api: openapi/kpn-sms-openapi.yml
operations:
  - "Sends single or bulk SMS"
generated: '2026-07-25'
method: generated
---

# Send an SMS over the KPN network

## 1. Get a token

POST `https://api-prd.kpn.com/oauth/client_credential/accesstoken?grant_type=client_credentials`
with the Client ID and Client Secret of your project. Use the returned token as
`Authorization: Bearer <access_token>` on every call. There are no scopes — access is granted by
adding the **SMS - KPN** product to your project in the developer portal.

## 2. Send the message

Call operation `Sends single or bulk SMS` — `POST https://api-prd.kpn.com/communication/kpn/sms/send`.

Body (`SmsKpn`):

- `messages[]` — one or more objects, each with required `content` and `mobile_number`
  (`06xxxxxxxx`, `+316xxxxxxxx`, `0031…` or `097…`; comma-separate numbers for bulk). 1–5000 items.
- `sender` — max 11 characters, defaults to `KPN`.
- `webhook_url` — where delivery reports are posted.
- Optional header `SubAccount` — leave blank if not applicable.

Hard limits from the documentation: **max 200 (messages × recipients) per call**, max **1000
characters** per message; over 160 characters the message is split into multiple SMS. `expirein`
must be at least 21 seconds for international traffic.

A 200 returns `SmsKpnSendResponse` with `document_id` (the tracking ID) and `status`. If
`document_id` is absent the request did not succeed.

## 3. Read the governance headers on every response

`quota-limit`, `quota-used`, `quota-interval`, `quota-time-unit`, `quota-reset-UTC` carry your
remaining quota; back off before you hit **429 Too Many Requests**. `api-version` tells you which
version served the call, and `sunset` carries deprecation details (it is `n/a` when the version is
current).

## 4. Verify the delivery-report webhook

KPN POSTs the delivery report to your `webhook_url` with four headers:

- `X-KPN-Webhook-Signature` — HMAC-SHA256 hex digest of the raw body
- `X-KPN-Webhook-Timestamp` — Unix epoch seconds, for replay protection
- `X-KPN-Webhook-Key-Id` — which signing key was used
- `X-KPN-Webhook-Attempt` — 1-based attempt number

Recompute the digest over the **raw body bytes** with your active signing key secret and compare in
constant time. Reject on mismatch. Delivery is **at-least-once** — 4 attempts at 0/60/120/240
seconds — and there is no idempotency key, so de-duplicate on `message_id`.

## 5. Interpret the result

Delivery status: `1` Delivered, `2` Queued, `3` Accepted, `4` Failed, `5` Rejected, `6` Expired.
Failure codes `001`–`030` are catalogued in `errors/kpn-sms-error-codes.yml`. Do not retry
recipient-permanent failures (`003`, `004`, `008`, `010`, `019`, `022`, `029`); `006`, `007`, `009`
and `011` are transient and may be retried later.

## Errors

Errors come back as `application/json` (never `application/problem+json`) in the
`ApiErrorResponse` envelope: `errorResponse.code`, `.message`, `.info`. See
`errors/kpn-problem-types.yml`.
