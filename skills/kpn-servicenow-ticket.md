---
name: Raise and track a KPN service ticket from your own ITSM
description: Create, update and follow KPN ServiceNow "Green" tickets and their tasks and attachments through the KPN ServiceNow Connect API.
api: openapi/kpn-servicenow-connect-openapi.yml
operations:
  - ticket-post
  - ticket-get
  - ticket-patch
  - ticket-list
  - ticketupdates-get
  - task-patch
  - get-attachment
generated: '2026-07-25'
method: generated
---

# Raise and track a KPN service ticket

Base URL `https://api-prd.kpn.com/network/kpn/servicenow`. OAuth 2.0 client-credentials bearer
token; add the **ServiceNow Customer Connect** product to your project.

## Create

`ticket-post` — `POST /Ticket`. Store the returned ticket identifier against your own incident
record; this is the only correlation key you get.

## Track

- `ticket-get` — `GET /Ticket` — full detail of one ticket
- `ticket-list` — `GET /ListOpenTickets` — everything currently open for your account
- `ticketupdates-get` — `GET /TicketUpdates` — poll for changes since your last sync; this is the
  intended synchronisation loop (KPN publishes no ticket webhook)
- `get-attachment` — `GET /GetAttachment/{attachment_id}` — pull an attachment referenced by a
  ticket or task

## Update

- `ticket-patch` — `PATCH /Ticket` — add worknotes, change state, resolve
- `task-patch` — `PATCH /Task` — update a task hanging off a ticket

## Operating rules

Poll `ticketupdates-get` on a fixed interval and honour the `quota-*` response headers rather than
tightening the loop after a 429. Errors are `application/json` in the KPN gateway envelope
(`transactionId`, `status`, `name`, `message`, `info`) — log `transactionId` when you contact
api_developer@kpn.com. There is no idempotency key on `ticket-post`: if a create times out, search
with `ticket-list` before creating again.
