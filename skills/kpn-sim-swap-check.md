---
name: Check for a recent SIM swap before a high-risk action (CAMARA)
description: Use the KPN Account Takeover Protection API to retrieve the last SIM swap date for a Dutch mobile line, or check whether a swap happened inside a lookback window, before allowing a password reset or payment.
api: openapi/kpn-sim-swap-openapi.yml
operations:
  - retrieveSimSwapDate
generated: '2026-07-25'
method: generated
---

# Check for a recent SIM swap

This is KPN's implementation of the CAMARA SIM Swap API — the definition points at
`https://github.com/camaraproject/` as its product documentation. KPN launched it for the Dutch
market with Odido and Vodafone under the COIN association and GSMA Open Gateway.

## 1. Get a token

Client-credentials token from
`https://api-prd.kpn.com/oauth/client_credential/accesstoken?grant_type=client_credentials`, then
`Authorization: Bearer <access_token>`. Add the **Account Takeover Protection** product to your
project first.

## 2. Call the check

Operation `retrieveSimSwapDate` — `POST https://api-prd.kpn.com/kpn/sim-swap/retrieve-date`.

```json
{ "phoneNumber": "+31612345678" }
```

The response carries the timestamp of the most recent SIM swap on that line. Compare it against
your own risk window (24h / 7d) rather than trusting a boolean.

## 3. Decide

Treat a swap inside the window as a **step-up signal**, not a hard block on its own: combine it
with your existing device and behavioural signals. This API is designed to gate password resets,
account recovery, payment confirmation and OTP delivery.

## Errors (CAMARA shape)

`400 INVALID_ARGUMENT`, `401 UNAUTHENTICATED`, `403 PERMISSION_DENIED`,
`404 SIM_SWAP.UNKNOWN_PHONE_NUMBER`, `409 CONFLICT`, `429 Too Many Requests`, `500 INTERNAL`,
`503 UNAVAILABLE`, `504 TIMEOUT`. The envelope is `application/json` with `error_code`, `message`
and `correlation_id` — log `correlation_id` for support.

## Testing

A SwaggerHub mock at `https://virtserver.swaggerhub.com/kpn/SimSwap-KPN/1.0.2` returns the schema
without credentials. KPN publishes no reserved test MSISDNs — the numbers in the definition are
documentation examples, not magic test values.
