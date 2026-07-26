---
name: Onboard and monitor a LoRaWAN device on the KPN LoRa network
description: Activate the API, create a device against a device profile and connectivity plan, then read frame, health and alarm telemetry with the KPN LoRa Device Management API.
api: openapi/kpn-lora-device-management-openapi.yml
operations:
  - Activation
  - Deviceprofilesretrieval
  - Connectivityplansretrieval
  - Devicecreation
  - Devicesretrieval
  - Deviceretrieval
  - Deviceupdate
  - Devicedeletion
  - Routingprofilescreation
  - Framestatisticsretrieval
  - Healthstatisticsretrieval
  - Devicealarmsretrieval
  - Devicealarmretrieval
  - Devicealarmacknowledgement
generated: '2026-07-25'
method: generated
---

# Onboard a LoRaWAN device on KPN

Base URL `https://api-prd.kpn.com/data/lora/thingpark`. OAuth 2.0 client-credentials bearer token;
add the **LoRa Device Management - KPN** product to your project.

## 1. Activate

`Activation` — `POST /activate`. Run once to activate API access for your account.

## 2. Pick the profiles the device will use

- `Deviceprofilesretrieval` — `GET /deviceProfiles`
- `Connectivityplansretrieval` — `GET /connectivityPlans`
- `Routingprofilesretrieval` — `GET /routingProfiles` (create one with
  `Routingprofilescreation` — `POST /routingProfiles` — if you need uplinks delivered somewhere new)

## 3. Create the device

`Devicecreation` — `POST /devices`, referencing the device profile, connectivity plan and routing
profile chosen above. Read it back with `Deviceretrieval` — `GET /devices/{deviceRef}` — and list
the fleet with `Devicesretrieval` — `GET /devices`. `Deviceupdate` (`PUT`) and `Devicedeletion`
(`DELETE`) manage the rest of the lifecycle.

## 4. Monitor

- `Framestatisticsretrieval` — `GET /deviceFrameStatistics` — uplink/downlink volumes
- `Healthstatisticsretrieval` — `GET /deviceHealthStatistics` — link quality
- `Devicealarmsretrieval` — `GET /deviceAlarms`, `Devicealarmretrieval` —
  `GET /deviceAlarms/{deviceAlarmRef}`
- `Devicealarmacknowledgement` — `POST /deviceAlarms/{deviceAlarmRef}/acks` — acknowledge an alarm
  once you have acted on it

## Operating rules

Watch `quota-limit` / `quota-used` on every response; fleet-wide list calls burn quota fastest —
page and cache instead of polling. There is no idempotency key: a retried `Devicecreation` after a
timeout can create a duplicate, so re-check with `Devicesretrieval` before retrying a write.
