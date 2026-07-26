---
name: Check broadband service and disturbances at a Dutch address
description: Look up real-time internet disturbance status and available speed/technology for a postcode and house number using the KPN Disturbance Check and Internet Speed Check APIs.
api: openapi/kpn-disturbance-check-openapi.yml
also_uses: openapi/kpn-internet-speed-check-openapi.yml
operations:
  - "GET /address"
  - "POST /offer (openapi/kpn-internet-speed-check-openapi.yml)"
generated: '2026-07-25'
method: generated
---

# Check service at a Dutch address

Two single-operation APIs answer the two questions an installer or a self-service flow asks about
an address. Both take postcode, house number and house extension.

> Neither definition publishes an `operationId`, so bind by method and path.

## 1. Is there a disturbance right now?

`GET https://api-prd.kpn.com/network/kpn/disturbance-check/address`
(`openapi/kpn-disturbance-check-openapi.yml`) — real-time disturbance status for the internet
service and technology at the address.

## 2. What speed and technology can this address get?

`POST https://api-prd.kpn.com/network/kpn/internet-speed-check/offer`
(`openapi/kpn-internet-speed-check-openapi.yml`) — the speed and technology available at the
address.

## Auth and operating rules

Client-credentials bearer token from
`https://api-prd.kpn.com/oauth/client_credential/accesstoken?grant_type=client_credentials`. Both
products declare a full-capability sandbox, HTTPS, OAuth and rate limiting, and are version-less:
send `api-version` to pin a version or omit it to get the latest.

Cache the speed/technology answer per address (it changes only when the network changes) but never
cache the disturbance answer — it is the live signal. Errors return the KPN gateway envelope
(`transactionId`, `status`, `name`, `message`, `info`) as `application/json`.

## Wholesale equivalent

Wholesale customers get the same class of address intelligence through Functional Product
Information and the Carrier Information Product — see
`openapi/kpn-wholesale-broadband-access-fpi-cip-openapi.yml`.
