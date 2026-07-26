---
name: Rotate a KPN webhook signing key without missing a delivery
description: Stage, reveal, activate, retire and delete an HMAC-SHA256 webhook signing key at organization, team or application level using the KPN Webhook Signing Keys API.
api: openapi/kpn-webhook-signing-keys-openapi.yml
operations:
  - createOrgSigningKey
  - listOrgSigningKeys
  - revealOrgSigningKeySecret
  - activateOrgSigningKey
  - retireOrgSigningKey
  - deleteOrgSigningKey
generated: '2026-07-25'
method: generated
---

# Rotate a webhook signing key

KPN signs every outbound webhook with HMAC-SHA256 and sends the digest in
`X-KPN-Webhook-Signature`, with `X-KPN-Webhook-Key-Id` naming the key used. Keys exist at three
levels — Organization, Team, Application — and KPN picks the most specific active key, falling back
Application → Team → Organization. An organization-level key is auto-provisioned on your first
delivery.

Base URL `https://api-prd.kpn.com/webhookconfigs-kpn`. You need an OAuth 2.0 bearer token and the
**WebhookConfigs-SigningKeys-KPN** product on your project.

## Key lifecycle

`staged` → `active` → `retiring` → `retired`. Only a retired key can be deleted.

## Steps (organization level)

1. `listOrgSigningKeys` — `GET /organizations/keys` — see what exists and which key is active.
2. `createOrgSigningKey` — `POST /organizations/keys` with `staged: true`. The current active key
   keeps signing; nothing breaks.
3. `revealOrgSigningKeySecret` — `GET /organizations/keys/reveal` — get the plaintext secret and
   configure your receiver to accept **both** the old and the new key.
4. `activateOrgSigningKey` — `POST /organizations/keys/{key_id}/activate` — the new key starts
   signing and the previously active key moves to `retiring` automatically.
5. Wait until every in-flight delivery has been verified (delivery is retried at 0/60/120/240s, so
   a few minutes is enough), then `retireOrgSigningKey` — `POST /organizations/keys/{key_id}/retire`.
6. `deleteOrgSigningKey` — `DELETE /organizations/keys/{key_id}`.

The same six operations exist for teams (`createTeamSigningKey`, `listTeamSigningKeys`,
`revealTeamSigningKeySecret`, `activateTeamSigningKey`, `retireTeamSigningKey`,
`deleteTeamSigningKey`) and applications (`createApplicationSigningKey`,
`listApplicationSigningKeys`, `revealApplicationSigningKeySecret`, `activateApplicationSigningKey`,
`retireApplicationSigningKey`, `deleteApplicationSigningKey`).

## Verifying on the receiver

Recompute the HMAC-SHA256 hex digest over the raw request body with the secret, compare with a
constant-time comparison, and check `X-KPN-Webhook-Timestamp` for replay. During rotation accept a
signature that matches either key; use `X-KPN-Webhook-Key-Id` to select.

## Related

Payload URL and field-exclusion settings live in a separate API — see
`openapi/kpn-webhook-privacy-config-manager-openapi.yml`. The `signing` block it returns is
read-only.
