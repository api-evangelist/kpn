# KPN

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Koninklijke KPN N.V. is the incumbent telecommunications and IT provider of the Netherlands, operating the country's national fixed (copper and fibre) and mobile networks and selling telephony, broadband, television, IoT connectivity and managed IT services to consumers, businesses and — through KPN Wholesale — to other operators. In the telecom API value chain KPN sits on the network-operator side, but it is a conspicuous exception to the carrier norm: rather than routing developers exclusively through aggregators, KPN runs a genuine self-serve developer portal at developer.kpn.com where anyone can register a free account, get a client ID and secret, test in a sandbox at no cost, and see per-transaction pricing, then upgrade to production via a KRN company number or an iDIN identity check. Thirty-four OpenAPI/Swagger definitions are published anonymously downloadable under KPN's public SwaggerHub organisation, all fronted by an Apigee-style gateway at api-prd.kpn.com with OAuth 2.0 client-credentials. KPN is listed in the official CAMARA landscape as an operator and, with Odido and Vodafone under the COIN association and GSMA Open Gateway, launched CAMARA-standard fraud-prevention APIs for the Dutch market in October 2025; its SIM Swap definition points explicitly at github.com/camaraproject as its product documentation. KPN is not an Aduna shareholder and does not reach developers through that JV. Notably, KPN also resells Vonage and Apidaze CPaaS products through its own portal — the aggregator layer appearing inside the carrier's own catalogue rather than the other way round.

**Areas:** Telecommunications · Netherlands · Mobile Network Operator · Broadband · Network APIs · CAMARA · Open Gateway · SIM Swap · Identity Verification · Messaging · SMS · Voice

## KPN on APIs.io

Everything profiled for KPN is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/kpn/](https://apis.io/providers/kpn/)** — or go straight to one of the APIs or properties below.

### APIs (103)

- [KPN GRIP API](https://apis.io/apis/kpn/kpn-grip/) — KPN Grip is a KPN identity and access management solution that acts as a central identity hub, letting developers integrate user registration,…
- [KPN PIM ID API](https://apis.io/apis/kpn/kpn-pim-id/) — KPN PiM ID generates tamper-proof, company-specific encrypted QR codes from validated customer data (POST /image on…
- [KPN SMS Campaigns API](https://apis.io/apis/kpn/kpn-sms-campaigns/) — Send and schedule bulk SMS campaigns over the KPN network. Documented on the KPN Developer portal; no public OpenAPI definition was found for this product…
- [KPN Email-to-SMS API](https://apis.io/apis/kpn/kpn-email-to-sms/) — Converts inbound email into SMS messages delivered over the KPN network. Documented on the KPN Developer portal; no public OpenAPI definition was found for…
- [KPN Account API](https://apis.io/apis/kpn/kpn-account-api/) — number management from accounts
- [KPN Activation API](https://apis.io/apis/kpn/kpn-activation-api/) — The Activation API from KPN — 1 operation(s) for activation.
- [KPN Alarm API](https://apis.io/apis/kpn/kpn-alarm-api/) — Alarm operations provide the ability to retrieve and acknowledge ThingPark device and base station alarms.
- [KPN Appliance.configure API](https://apis.io/apis/kpn/kpn-appliance-configure-api/) — The appliance.configure API from KPN — 51 operation(s) for appliance.configure.
- [KPN Appliance.monitor API](https://apis.io/apis/kpn/kpn-appliance-monitor-api/) — The appliance.monitor API from KPN — 13 operation(s) for appliance.monitor.
- [KPN Application API](https://apis.io/apis/kpn/kpn-application-api/) — Application-scope webhook configuration — webhook URL and field exclusions. Highest precedence — overrides both team and organization config for this…
- [KPN Application Keys API](https://apis.io/apis/kpn/kpn-application-keys-api/) — Signing keys at application scope. Highest precedence — overrides both team and org keys for deliveries belonging to this specific application.
- [KPN Applications API](https://apis.io/apis/kpn/kpn-applications-api/) — Application related resource management
- [KPN Attachment API](https://apis.io/apis/kpn/kpn-attachment-api/) — The Attachment API from KPN — 1 operation(s) for attachment.
- [KPN Authentication API](https://apis.io/apis/kpn/kpn-authentication-api/) — Authentication endpoints for token management
- [KPN Authorization API](https://apis.io/apis/kpn/kpn-authorization-api/) — Authorization policy enforcement endpoints
- [KPN Autologin API](https://apis.io/apis/kpn/kpn-autologin-api/) — The Autologin API from KPN — 1 operation(s) for autologin.
- [KPN Callback API](https://apis.io/apis/kpn/kpn-callback-api/) — The Callback API from KPN — 1 operation(s) for callback.
- [KPN Cases API](https://apis.io/apis/kpn/kpn-cases-api/) — All about case handling
- [KPN Catalog API](https://apis.io/apis/kpn/kpn-catalog-api/) — Logical grouping of content
- [KPN Cellular Gateway.configure API](https://apis.io/apis/kpn/kpn-cellulargateway-configure-api/) — The cellularGateway.configure API from KPN — 15 operation(s) for cellulargateway.configure.
- [KPN Cellular Gateway.monitor API](https://apis.io/apis/kpn/kpn-cellulargateway-monitor-api/) — The cellularGateway.monitor API from KPN — 1 operation(s) for cellulargateway.monitor.
- [KPN Config API](https://apis.io/apis/kpn/kpn-config-api/) — The Config API from KPN — 1 operation(s) for config.
- [KPN Configuration API](https://apis.io/apis/kpn/kpn-configuration-api/) — All about configuring Tracebuzz
- [KPN Contract Validation API](https://apis.io/apis/kpn/kpn-contract-validation-api/) — Contract access validation endpoints
- [KPN Data Consumer API](https://apis.io/apis/kpn/kpn-dataconsumer-api/) — The DataConsumer API from KPN — 2 operation(s) for dataconsumer.
- [KPN Data Consumer Demo API](https://apis.io/apis/kpn/kpn-dataconsumerdemo-api/) — The DataConsumerDemo API from KPN — 2 operation(s) for dataconsumerdemo.
- [KPN Default API](https://apis.io/apis/kpn/kpn-default-api/) — The default API from KPN — 6 operation(s) for default.
- [KPN Device API](https://apis.io/apis/kpn/kpn-device-api/) — Device operations provide the ability to manage ThingPark devices, device profiles, routing profiles, and connectivity plans.
- [KPN Devices API](https://apis.io/apis/kpn/kpn-devices-api/) — The Devices API from KPN — 1 operation(s) for devices.
- [KPN Device Security API](https://apis.io/apis/kpn/kpn-devicesecurity-api/) — Device security operations provide the ability to manage AS keys and HSM groups for enhanced message encryption.
- [KPN Emailing API](https://apis.io/apis/kpn/kpn-emailing-api/) — The Emailing API from KPN — 1 operation(s) for emailing.
- [KPN Endpoint API](https://apis.io/apis/kpn/kpn-endpoint-api/) — The endpoint API from KPN — 4 operation(s) for endpoint.
- [KPN Events API](https://apis.io/apis/kpn/kpn-events-api/) — The Events API from KPN — 2 operation(s) for events.
- [KPN Identitygroup API](https://apis.io/apis/kpn/kpn-identitygroup-api/) — The identitygroup API from KPN — 1 operation(s) for identitygroup.
- [KPN Insight.configure API](https://apis.io/apis/kpn/kpn-insight-configure-api/) — The insight.configure API from KPN — 3 operation(s) for insight.configure.
- [KPN Insight.monitor API](https://apis.io/apis/kpn/kpn-insight-monitor-api/) — The insight.monitor API from KPN — 1 operation(s) for insight.monitor.
- [KPN Insights API](https://apis.io/apis/kpn/kpn-insights-api/) — The Insights API from KPN — 1 operation(s) for insights.
- [KPN Internaluser API](https://apis.io/apis/kpn/kpn-internaluser-api/) — The internaluser API from KPN — 1 operation(s) for internaluser.
- [KPN Item API](https://apis.io/apis/kpn/kpn-item-api/) — Detailed descriptions of the content
- [KPN JWT API](https://apis.io/apis/kpn/kpn-jwt-api/) — Call to generate JWT.
- [KPN Meetings API](https://apis.io/apis/kpn/kpn-meetings-api/) — The Meetings API from KPN — 2 operation(s) for meetings.
- [KPN Messages API](https://apis.io/apis/kpn/kpn-messages-api/) — The Messages API from KPN — 3 operation(s) for messages.
- [KPN Networks API](https://apis.io/apis/kpn/kpn-networks-api/) — The Networks API from KPN — 1 operation(s) for networks.
- [KPN Number API](https://apis.io/apis/kpn/kpn-number-api/) — numbers operations
- [KPN Organization API](https://apis.io/apis/kpn/kpn-organization-api/) — Organization-scope webhook configuration. Applies to all teams and applications in your organization unless a team or application config overrides it.
- [KPN Organization Keys API](https://apis.io/apis/kpn/kpn-organization-keys-api/) — Signing keys at organization scope. Applied to all webhook deliveries in your organization unless a team or application key overrides them. KPN…
- [KPN Organizations API](https://apis.io/apis/kpn/kpn-organizations-api/) — The Organizations API from KPN — 2 operation(s) for organizations.
- [KPN Packages API](https://apis.io/apis/kpn/kpn-packages-api/) — The Packages API from KPN — 2 operation(s) for packages.
- [KPN Parties API](https://apis.io/apis/kpn/kpn-parties-api/) — Party and participant management endpoints
- [KPN Personal API](https://apis.io/apis/kpn/kpn-personal-api/) — The Personal API from KPN — 3 operation(s) for personal.
- [KPN Polling API](https://apis.io/apis/kpn/kpn-polling-api/) — The Polling API from KPN — 1 operation(s) for polling.
- [KPN Register webhook - Demo testing ONLY API](https://apis.io/apis/kpn/kpn-register-webhook-demo-testing-only-api/) — The Register webhook - Demo testing ONLY API from KPN — 1 operation(s) for register webhook - demo testing only.
- [KPN Request API](https://apis.io/apis/kpn/kpn-request-api/) — The Request API from KPN — 2 operation(s) for request.
- [KPN Rest Address Controller API](https://apis.io/apis/kpn/kpn-rest-address-controller-api/) — Rest Address Controller
- [KPN Rest Block Sim Controller API](https://apis.io/apis/kpn/kpn-rest-block-sim-controller-api/) — Rest Block Sim Controller
- [KPN Rest Business Voice Mail Controller API](https://apis.io/apis/kpn/kpn-rest-business-voice-mail-controller-api/) — Rest Business Voice Mail Controller
- [KPN Rest Contract Controller API](https://apis.io/apis/kpn/kpn-rest-contract-controller-api/) — Rest Contract Controller
- [KPN Rest Contract Terminate Controller API](https://apis.io/apis/kpn/kpn-rest-contract-terminate-controller-api/) — Rest Contract Terminate Controller
- [KPN Rest Contracting Controller API](https://apis.io/apis/kpn/kpn-rest-contracting-controller-api/) — Rest Contracting Controller
- [KPN Rest Hardware Enrollment Controller API](https://apis.io/apis/kpn/kpn-rest-hardware-enrollment-controller-api/) — Rest Hardware Enrollment Controller
- [KPN Rest Hierarchy Controller API](https://apis.io/apis/kpn/kpn-rest-hierarchy-controller-api/) — Rest Hierarchy Controller
- [KPN Rest Invoice Controller API](https://apis.io/apis/kpn/kpn-rest-invoice-controller-api/) — Rest Invoice Controller
- [KPN Rest Order Controller API](https://apis.io/apis/kpn/kpn-rest-order-controller-api/) — Rest Order Controller
- [KPN Rest Separate Fixed Mobile Controller API](https://apis.io/apis/kpn/kpn-rest-separate-fixed-mobile-controller-api/) — Rest Separate Fixed Mobile Controller
- [KPN Rest Subscriber Controller API](https://apis.io/apis/kpn/kpn-rest-subscriber-controller-api/) — Rest Subscriber Controller
- [KPN Rest Template Controller API](https://apis.io/apis/kpn/kpn-rest-template-controller-api/) — Rest Template Controller
- [KPN Rest Threshold Controller API](https://apis.io/apis/kpn/kpn-rest-threshold-controller-api/) — Rest Threshold Controller
- [KPN Rest Track And Trace Controller API](https://apis.io/apis/kpn/kpn-rest-track-and-trace-controller-api/) — Rest Track And Trace Controller
- [KPN Rest User Controller API](https://apis.io/apis/kpn/kpn-rest-user-controller-api/) — Rest User Controller
- [KPN Results API](https://apis.io/apis/kpn/kpn-results-api/) — All about managing results
- [KPN Retrieve job result API](https://apis.io/apis/kpn/kpn-retrieve-job-result-api/) — The Retrieve job result API from KPN — 3 operation(s) for retrieve job result.
- [KPN Retrieve SIM swap date API](https://apis.io/apis/kpn/kpn-retrieve-sim-swap-date-api/) — The Retrieve SIM swap date API from KPN — 1 operation(s) for retrieve sim swap date.
- [KPN Retrieve transcription API](https://apis.io/apis/kpn/kpn-retrieve-transcription-api/) — To retrieve transcritions, check the processing status with your unique **job_id**. Please do not use intervals that are shorter than 10 seconds to check…
- [KPN Routing API](https://apis.io/apis/kpn/kpn-routing-api/) — The Routing API from KPN — 2 operation(s) for routing.
- [KPN Send SMS API](https://apis.io/apis/kpn/kpn-send-sms-api/) — The Send SMS API from KPN — 1 operation(s) for send sms.
- [KPN Service Consumer Contracts API](https://apis.io/apis/kpn/kpn-service-consumer-contracts-api/) — Contract access for service consumers (read-only operations)
- [KPN Service Provider Contracts API](https://apis.io/apis/kpn/kpn-service-provider-contracts-api/) — Contract management for service providers (full CRUD operations)
- [KPN Service Provider Parties API](https://apis.io/apis/kpn/kpn-service-provider-parties-api/) — Service provider view of consumer parties and their contracts
- [KPN Session API](https://apis.io/apis/kpn/kpn-session-api/) — The Session API from KPN — 1 operation(s) for session.
- [KPN Sites API](https://apis.io/apis/kpn/kpn-sites-api/) — The Sites API from KPN — 1 operation(s) for sites.
- [KPN Start engineering job API](https://apis.io/apis/kpn/kpn-start-engineering-job-api/) — The Start engineering job API from KPN — 2 operation(s) for start engineering job.
- [KPN Statistics API](https://apis.io/apis/kpn/kpn-statistics-api/) — The Statistics API from KPN — 2 operation(s) for statistics.
- [KPN Subscription API](https://apis.io/apis/kpn/kpn-subscription-api/) — The Subscription API from KPN — 1 operation(s) for subscription.
- [KPN Switch.configure API](https://apis.io/apis/kpn/kpn-switch-configure-api/) — The switch.configure API from KPN — 47 operation(s) for switch.configure.
- [KPN Switch.monitor API](https://apis.io/apis/kpn/kpn-switch-monitor-api/) — The switch.monitor API from KPN — 9 operation(s) for switch.monitor.
- [KPN Task API](https://apis.io/apis/kpn/kpn-task-api/) — The Task API from KPN — 1 operation(s) for task.
- [KPN Team API](https://apis.io/apis/kpn/kpn-team-api/) — Team-scope webhook configuration — webhook URL and field exclusions. Overrides the organization config for all applications in your team unless an…
- [KPN Team Keys API](https://apis.io/apis/kpn/kpn-team-keys-api/) — Signing keys at team scope. Override the organization key for all deliveries in your team unless an application key is configured.
- [KPN Ticket API](https://apis.io/apis/kpn/kpn-ticket-api/) — The Ticket API from KPN — 3 operation(s) for ticket.
- [KPN Token API](https://apis.io/apis/kpn/kpn-token-api/) — The Token API from KPN — 1 operation(s) for token.
- [KPN Upload audio API](https://apis.io/apis/kpn/kpn-upload-audio-api/) — Uploads an audio file and start a new analytics job.
- [KPN User Management API](https://apis.io/apis/kpn/kpn-user-management-api/) — The User Management API from KPN — 1 operation(s) for user management.
- [KPN Users API](https://apis.io/apis/kpn/kpn-users-api/) — The Users API from KPN — 4 operation(s) for users.
- [KPN Verify API](https://apis.io/apis/kpn/kpn-verify-api/) — The Verify API from KPN — 4 operation(s) for verify.
- [KPN Voice API](https://apis.io/apis/kpn/kpn-voice-api/) — Call related resource management
- [KPN VoIP SIP API](https://apis.io/apis/kpn/kpn-voip-sip-api-api/) — The VoIP SIP API API from KPN — 3 operation(s) for voip sip api.
- [KPN Webhook API](https://apis.io/apis/kpn/kpn-webhook-api/) — The Webhook API from KPN — 1 operation(s) for webhook.
- [KPN Wireless.configure API](https://apis.io/apis/kpn/kpn-wireless-configure-api/) — The wireless.configure API from KPN — 37 operation(s) for wireless.configure.
- [KPN Wireless.monitor API](https://apis.io/apis/kpn/kpn-wireless-monitor-api/) — The wireless.monitor API from KPN — 33 operation(s) for wireless.monitor.
- [KPN XML Scripting API](https://apis.io/apis/kpn/kpn-xml-scripting-api-api/) — The XML Scripting API API from KPN — 3 operation(s) for xml scripting api.
- [KPN Your Active Webhook API](https://apis.io/apis/kpn/kpn-your-active-webhook-api/) — The Your Active Webhook API from KPN — 1 operation(s) for your active webhook.
- [KPN Endpoint Group API](https://apis.io/apis/kpn/kpn-endpoint-group-api/) — The Endpoint Group API from KPN — 1 operation(s) for endpoint group.
- [KPN Graph QL API](https://apis.io/apis/kpn/kpn-graph-ql-api/) — The Graph QL API from KPN — 1 operation(s) for graph ql.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Kpn Webhooks](https://apis.io/asyncapis/kpn/kpn-webhooks/)

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [kpn](https://apis.io/servers/kpn/kpn/)

#### Collections (33)

Postman and Open Collection request collections.

- [Apidaze Voice - VoIP Innovations](https://apis.io/collections/kpn/open-apidaze-voice/)
- [Disturbance Check - KPN](https://apis.io/collections/kpn/open-kpn-disturbance-check/)
- [FIAM-KPN](https://apis.io/collections/kpn/open-kpn-fiam/)
- [FIAM – Eneco Data Products](https://apis.io/collections/kpn/open-kpn-fiam-eneco-data-products/)
- [High-Level Design FTTx](https://apis.io/collections/kpn/open-kpn-high-level-design-ftth/)
- [Internet Speed Check - KPN](https://apis.io/collections/kpn/open-kpn-internet-speed-check/)
- [ISE - KPN](https://apis.io/collections/kpn/open-kpn-ise/)
- [LoRa Device Management - KPN](https://apis.io/collections/kpn/open-kpn-lora-device-management/)
- [Match - KPN](https://apis.io/collections/kpn/open-kpn-match/)
- [MobileServicesManagement-KPN](https://apis.io/collections/kpn/open-kpn-mobile-services-management/)
- [Number Verify - KPN](https://apis.io/collections/kpn/open-kpn-number-verify/)
- [KPN SD-LAN SD-WAN Network View API](https://apis.io/collections/kpn/open-kpn-sd-lan-sd-wan-network-view/)
- [ServiceNow Customer Connect](https://apis.io/collections/kpn/open-kpn-servicenow-connect/)
- [SIM Swap](https://apis.io/collections/kpn/open-kpn-sim-swap/)
- [Inbound SMS - KPN](https://apis.io/collections/kpn/open-kpn-sms-inbound/)
- [TV Guide - KPN](https://apis.io/collections/kpn/open-kpn-tv-guide/)
- [Webhook Privacy Configuration - KPN](https://apis.io/collections/kpn/open-kpn-webhook-privacy-config-manager/)
- [Webhook Signing Keys - KPN](https://apis.io/collections/kpn/open-kpn-webhook-signing-keys/)
- [Wholesale Broadband Access](https://apis.io/collections/kpn/open-kpn-wholesale-broadband-access-fpi-cip/)
- [WBA APIs](https://apis.io/collections/kpn/open-kpn-wholesale-wba/)
- [Chat and Messaging - Parley](https://apis.io/collections/kpn/open-parley-secure-messenger/)
- [Knowledge Management – Polly.help](https://apis.io/collections/kpn/open-pollyhelp-knowledge-management/)
- [Registered E-mail - Registered E-mail](https://apis.io/collections/kpn/open-registered-email/)
- [SocialMediaWebcare - Tracebuzz](https://apis.io/collections/kpn/open-tracebuzz-social-media-webcare/)
- [Messages - Vonage](https://apis.io/collections/kpn/open-vonage-messages/)
- …and 8 more published on APIs.io

#### Overlays (34)

OpenAPI overlays, including conversational phrasing for each operation.

- [Kpn Apidaze Voice Overlay](https://apis.io/overlays/kpn/kpn-apidaze-voice-overlay/)
- [Kpn Disturbance Check Overlay](https://apis.io/overlays/kpn/kpn-disturbance-check-overlay/)
- [Kpn Fiam Eneco Data Products Overlay](https://apis.io/overlays/kpn/kpn-fiam-eneco-data-products-overlay/)
- [Kpn Fiam Overlay](https://apis.io/overlays/kpn/kpn-fiam-overlay/)
- [Kpn High Level Design Ftth Overlay](https://apis.io/overlays/kpn/kpn-high-level-design-ftth-overlay/)
- [Kpn Internet Speed Check Overlay](https://apis.io/overlays/kpn/kpn-internet-speed-check-overlay/)
- [Kpn Ise Overlay](https://apis.io/overlays/kpn/kpn-ise-overlay/)
- [Kpn Lora Device Management Overlay](https://apis.io/overlays/kpn/kpn-lora-device-management-overlay/)
- [Kpn Match Overlay](https://apis.io/overlays/kpn/kpn-match-overlay/)
- [Kpn Mobile Services Management Overlay](https://apis.io/overlays/kpn/kpn-mobile-services-management-overlay/)
- [Kpn Number Verify Overlay](https://apis.io/overlays/kpn/kpn-number-verify-overlay/)
- [Kpn Parley Secure Messenger Overlay](https://apis.io/overlays/kpn/kpn-parley-secure-messenger-overlay/)
- [Kpn Pollyhelp Knowledge Management Overlay](https://apis.io/overlays/kpn/kpn-pollyhelp-knowledge-management-overlay/)
- [Kpn Registered Email Overlay](https://apis.io/overlays/kpn/kpn-registered-email-overlay/)
- [Kpn Sd Lan Sd Wan Network View Overlay](https://apis.io/overlays/kpn/kpn-sd-lan-sd-wan-network-view-overlay/)
- [Kpn Servicenow Connect Overlay](https://apis.io/overlays/kpn/kpn-servicenow-connect-overlay/)
- [Kpn Sim Swap Overlay](https://apis.io/overlays/kpn/kpn-sim-swap-overlay/)
- [Kpn Sms Inbound Overlay](https://apis.io/overlays/kpn/kpn-sms-inbound-overlay/)
- [Kpn Sms Overlay](https://apis.io/overlays/kpn/kpn-sms-overlay/)
- [Kpn Tracebuzz Social Media Webcare Overlay](https://apis.io/overlays/kpn/kpn-tracebuzz-social-media-webcare-overlay/)
- [Kpn Tv Guide Overlay](https://apis.io/overlays/kpn/kpn-tv-guide-overlay/)
- [Kpn Vonage Messages Overlay](https://apis.io/overlays/kpn/kpn-vonage-messages-overlay/)
- [Kpn Vonage Number Insight Overlay](https://apis.io/overlays/kpn/kpn-vonage-number-insight-overlay/)
- [Kpn Vonage Phone Numbers Overlay](https://apis.io/overlays/kpn/kpn-vonage-phone-numbers-overlay/)
- [Kpn Vonage Sms Overlay](https://apis.io/overlays/kpn/kpn-vonage-sms-overlay/)
- …and 9 more published on APIs.io

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Kpn Authentication](https://apis.io/security/kpn/kpn-authentication/)
- [Kpn Domain Security](https://apis.io/security/kpn/kpn-domain-security/)
- [Kpn Vulnerability Disclosure](https://apis.io/security/kpn/kpn-vulnerability-disclosure/)

#### OAuth scopes (1)

The permissions the API asks for.

- [Kpn Scopes](https://apis.io/scopes/kpn/kpn-scopes/)

#### Plans and pricing (2)

Published plans, tiers and prices.

- [Kpn Plans Pricing](https://apis.io/plans/kpn/kpn-plans-pricing/)
- [Kpn Price Estimates](https://apis.io/plans/kpn/kpn-price-estimates/)

#### Rate limits (1)

Published request limits.

- [Kpn Rate Limits](https://apis.io/rate-limits/kpn/kpn-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.kpn.com/)
- [Documentation](https://developer.kpn.com/documentation)
- [Getting started](https://developer.kpn.com/page/getting-started)
- [API reference](https://app.swaggerhub.com/search?owner=kpn)
- [Pricing](https://developer.kpn.com/products/kpn-sms-api)
- [Sign up](https://developer.kpn.com/dashboard/register)
- [Support](https://developer.kpn.com/support)
- [Blog](https://developer.kpn.com/blog)
- [Security](https://developer.kpn.com/page/responsible-disclosure)
- [Terms of service](https://developer.kpn.com/page/legal)
- [Privacy policy](https://www.kpn.com/algemeen/missie-en-privacy-statement/privacy-statement.htm)
- [GitHub](https://github.com/kpn)
- [Status](https://developer.kpn.com/status)

## API Evangelist rating

**Kin Score 62.4** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 69.6 |
| Contract quality | 59.4 |
| Contract governance | 18.2 |
| Operational transparency | 86.8 |
| Developer ergonomics | 60.1 |
| Access clarity | 59.2 |

**Agent readiness 35.1** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | negotiable (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | mostly |

**Regulatory alignment 47.1** — Telecommunications

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/kpn/](https://apis.io/providers/kpn/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for KPN: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/kpn/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
