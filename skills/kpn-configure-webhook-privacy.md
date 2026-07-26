---
name: Configure webhook delivery URL and payload privacy per application
description: Set the webhook URL and control which fields KPN includes in outbound payloads at organization, team or application scope with the KPN Webhook Privacy Config Manager API.
api: openapi/kpn-webhook-privacy-config-manager-openapi.yml
operations:
  - getOrganizationWebhookConfig
  - updateOrganizationWebhookConfig
  - createTeamWebhookConfig
  - getTeamWebhookConfig
  - updateTeamWebhookConfig
  - deleteTeamWebhookConfig
  - createApplicationWebhookConfig
  - getApplicationWebhookConfig
  - updateApplicationWebhookConfig
  - deleteApplicationWebhookConfig
generated: '2026-07-25'
method: generated
---

# Configure webhook delivery and payload privacy

Base URL `https://api-prd.kpn.com/webhookconfigs-kpn`, OAuth 2.0 bearer token required.

Configuration cascades **Application → Team → Organization**: the most specific config wins. Set
sane defaults at organization level and override only where one application needs something else.

## Read the effective configuration

- `getOrganizationWebhookConfig` — `GET /organizations`
- `getTeamWebhookConfig` — `GET /teams`
- `getApplicationWebhookConfig` — `GET /applications`

The returned `signing` block is **read-only** — rotate keys with the Webhook Signing Keys API
(`skills/kpn-rotate-webhook-signing-key.md`).

## Set the delivery URL and field exclusions

`privacy_config.excluded_fields` maps a service name to the list of fields to omit from that
service's outbound payloads. Any field not listed is included; an empty or absent map means every
field is sent. To hide the recipient number and body from SMS delivery reports:

```json
{ "privacy_config": { "excluded_fields": { "sms_dlr": ["RecipientPhonenumber", "Message"] } } }
```

- Organization: `updateOrganizationWebhookConfig` — `PUT /organizations`
- Team: `createTeamWebhookConfig` / `updateTeamWebhookConfig` / `deleteTeamWebhookConfig`
- Application: `createApplicationWebhookConfig` / `updateApplicationWebhookConfig` /
  `deleteApplicationWebhookConfig`

Deleting a team or application config falls back to the broader scope rather than turning
webhooks off.

## Before you exclude a field

Exclusion is a privacy control, not a security control — signatures still cover only what is sent.
If you drop `Message` or `RecipientPhonenumber` from `sms_dlr`, your reconciliation must key on
`message_id` / `document_id` instead.
