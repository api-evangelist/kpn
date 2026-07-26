# KPN (kpn)

Koninklijke KPN N.V. is the incumbent telecommunications and IT provider of the Netherlands, operating the country's national fixed (copper and fibre) and mobile networks and selling telephony, broadband, television, IoT connectivity and managed IT services to consumers, businesses and — through KPN Wholesale — to other operators. In the telecom API value chain KPN sits on the network-operator side, but it is a conspicuous exception to the carrier norm: rather than routing developers exclusively through aggregators, KPN runs a genuine self-serve developer portal at developer.kpn.com where anyone can register a free account, get a client ID and secret, test in a sandbox at no cost, and see per-transaction pricing, then upgrade to production via a KRN company number or an iDIN identity check. Thirty-four OpenAPI/Swagger definitions are published anonymously downloadable under KPN's public SwaggerHub organisation, all fronted by an Apigee-style gateway at api-prd.kpn.com with OAuth 2.0 client-credentials. KPN is listed in the official CAMARA landscape as an operator and, with Odido and Vodafone under the COIN association and GSMA Open Gateway, launched CAMARA-standard fraud-prevention APIs for the Dutch market in October 2025; its SIM Swap definition points explicitly at github.com/camaraproject as its product documentation. KPN is not an Aduna shareholder and does not reach developers through that JV. Notably, KPN also resells Vonage and Apidaze CPaaS products through its own portal — the aggregator layer appearing inside the carrier's own catalogue rather than the other way round.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/kpn/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/kpn/refs/heads/main/apis.yml)

## Tags

- Telecommunications
- Netherlands
- Mobile Network Operator
- Broadband
- Network APIs
- CAMARA
- Open Gateway
- SIM Swap
- Identity Verification
- Messaging
- SMS
- Voice
- IoT
- LoRaWAN
- Fiber
- Wholesale
- 5G
- Europe

## Timestamps

- **Created:** 2026-07-25
- **Modified:** 2026-07-25

## Developer Surface

- **Developer portal:** [https://developer.kpn.com/](https://developer.kpn.com/) — HTTP 200, a real self-serve portal. Free account, free sandbox testing, issued `client_id`/`client_secret`, published per-transaction pricing. Production access requires a KPN Registration Number (KRN) or an iDIN identity check.
- **Open Gateway:** `opengateway.kpn.com` redirects to the same developer portal.
- **Gateway host:** `https://api-prd.kpn.com`, Apigee-style, OAuth 2.0 client credentials at `/oauth/client_credential/accesstoken`. No CIBA anywhere; no OIDC discovery document served.
- **OpenAPI:** 34 definitions harvested verbatim from the public SwaggerHub organisation [`kpn`](https://app.swaggerhub.com/search?owner=kpn) (456 paths, 645 operations; 28 OpenAPI 3.x, 6 Swagger 2.0). All downloaded anonymously at HTTP 200 and validated.
- **CAMARA:** KPN is listed in the official [CAMARA landscape](https://github.com/camaraproject/camara-landscape/blob/main/landscape.yml) under *Operation / Operators*, and launched CAMARA fraud-prevention APIs for the Dutch market with Odido and Vodafone under GSMA Open Gateway and the COIN association on 2025-10-30. **SIM Swap** ships as a genuinely CAMARA-shaped, downloadable, self-serve-purchasable definition (`externalDocs` points at github.com/camaraproject). **Number Verification** and **KYC Match** are real priced products, but the specs KPN publishes for them are its own pre-CAMARA / GSMA Mobile Connect contracts.
- **Aduna:** not a partner. KPN reaches developers directly.
- **TM Forum:** no Open API conformance certification found; the BSS/OSS-shaped surfaces are proprietary contracts.
- **3GPP:** no NEF/SCEF surface, no network-slicing API, no edge/MEC API.
- **Webhooks:** yes — dedicated Webhook Signing Keys (HMAC-SHA256) and Webhook Privacy Config Manager APIs. No AsyncAPI.
- **SDKs:** none first-party on npm or PyPI. A public [Postman workspace](https://www.postman.com/kpndeveloper) is the documented client path. The portal documents a `github.com/kpn-developer` spec repo that now has **zero public repositories**.
- **Channel inversion:** KPN resells CPaaS rather than depending on it — seven harvested specs are Vonage/Nexmo and Apidaze APIs proxied through KPN's own gateway.

## APIs (38)

### KPN Number Verify API

With KPN Number Verify, you can quickly check whether the mobile number someone provides is the same as their SIM card.

- **Human URL:** [https://developer.kpn.com/products/kpn-number-verify](https://developer.kpn.com/products/kpn-number-verify)
- **Base URL:** `https://api-prd.kpn.com/communication/kpn/numberverify`

#### Tags

- Identity
- Verification
- Number Verification
- Mobile
- Network APIs

#### Properties

- [Documentation](https://developer.kpn.com/products/kpn-number-verify)
- [Documentation](https://developer.kpn.com/documentation/kpn-number-verify-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/numberverify-kpn)
- [OpenAPI](openapi/kpn-number-verify-openapi.yml)

### KPN SIM Swap API (Account Takeover Protection)

The SIM swap API provides a programmable interface for developers and other users (capabilities consumers) to request the last date of a SIM swap performed on the mobile line, or, to check whether a SIM swap has been performed during a past period.

- **Human URL:** [https://developer.kpn.com/products/kpn-account-takeover-protection](https://developer.kpn.com/products/kpn-account-takeover-protection)
- **Base URL:** `https://api-prd.kpn.com/kpn/sim-swap`

#### Tags

- Security
- SIM Swap
- Anti-Fraud
- CAMARA
- Network APIs

#### Properties

- [Documentation](https://developer.kpn.com/products/kpn-account-takeover-protection)
- [Documentation](https://developer.kpn.com/documentation/kpn-account-takeover-protection-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/simswap-kpn)
- [OpenAPI](openapi/kpn-sim-swap-openapi.yml)

### KPN Match API

Seamlessly check and verify an identity.

- **Human URL:** [https://developer.kpn.com/products/kpn-match](https://developer.kpn.com/products/kpn-match)
- **Base URL:** `https://api-prd.kpn.com/communication/kpn/match`

#### Tags

- Identity
- KYC
- Verification
- Mobile Connect

#### Properties

- [Documentation](https://developer.kpn.com/products/kpn-match)
- [Documentation](https://developer.kpn.com/documentation/kpn-match-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/match-kpn)
- [OpenAPI](openapi/kpn-match-openapi.yml)

### KPN SMS API

Send SMS through the KPN network.

- **Human URL:** [https://developer.kpn.com/products/kpn-sms-api](https://developer.kpn.com/products/kpn-sms-api)
- **Base URL:** `https://api-prd.kpn.com/communication/kpn/sms`

#### Tags

- Messaging
- SMS

#### Properties

- [Documentation](https://developer.kpn.com/products/kpn-sms-api)
- [Documentation](https://developer.kpn.com/documentation/kpn-sms-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/sms-kpn)
- [OpenAPI](openapi/kpn-sms-openapi.yml)

### KPN SMS Inbound API

This API is designed to inform users about the response schema they will receive on their webhook when an SMS message is sent to their virtual number. The API provides details of the message format that includes sender, recipient, message ID, content, timestamp, and type of the SMS.

- **Human URL:** [https://developer.kpn.com/products/kpn-sms-api](https://developer.kpn.com/products/kpn-sms-api)
- **Base URL:** `https://api-prd.kpn.com`

#### Tags

- Messaging
- SMS
- Webhooks

#### Properties

- [Documentation](https://developer.kpn.com/products/kpn-sms-api)
- [Documentation](https://developer.kpn.com/documentation/kpn-sms-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/sms-inbound)
- [OpenAPI](openapi/kpn-sms-inbound-openapi.yml)

### KPN Mobile Services Management API

MobileServicesManagement APIs ---

- **Human URL:** [https://developer.kpn.com/products/kpn-mobile-services-management-api](https://developer.kpn.com/products/kpn-mobile-services-management-api)
- **Base URL:** `https://api-prd.kpn.com/mobile/kpn/mobileservices`

#### Tags

- Mobile
- Fleet Management
- Ordering
- BSS

#### Properties

- [Documentation](https://developer.kpn.com/products/kpn-mobile-services-management-api)
- [Documentation](https://developer.kpn.com/documentation/kpn-mobile-services-management-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/mobileservicesmanagement-kpn)
- [OpenAPI](openapi/kpn-mobile-services-management-openapi.yml)

### KPN FIAM API

A collection of crates for federated identity and access management

- **Human URL:** [https://developer.kpn.com/products/federated-identity-and-access-management](https://developer.kpn.com/products/federated-identity-and-access-management)
- **Base URL:** `https://api-prd.kpn.com/fiam`

#### Tags

- Identity
- Federated Identity
- Access Management
- Data Spaces

#### Properties

- [Documentation](https://developer.kpn.com/products/federated-identity-and-access-management)
- [Documentation](https://developer.kpn.com/documentation/fiam-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/fiam-kpn)
- [OpenAPI](openapi/kpn-fiam-openapi.yml)

### KPN FIAM Eneco Data Products API

FIAM – Eneco Data Products

- **Human URL:** [https://developer.kpn.com/products/fiam-eneco-data-products](https://developer.kpn.com/products/fiam-eneco-data-products)
- **Base URL:** `https://api-acc.enecogroup.com/`

#### Tags

- Identity
- Data Sharing
- Energy

#### Properties

- [Documentation](https://developer.kpn.com/products/fiam-eneco-data-products)
- [Documentation](https://developer.kpn.com/documentation/eneco-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/fiam-eneco-data-products)
- [OpenAPI](openapi/kpn-fiam-eneco-data-products-openapi.yml)

### KPN Disturbance Check API

This API allows you to check the disturbance of the internet and the technology at an address. The API takes the postcode, house number and house extension, sends the request to the backend to retrieve real time information about the internet and technology service at the address.

- **Human URL:** [https://developer.kpn.com/products/kpn-disturbance-check-api](https://developer.kpn.com/products/kpn-disturbance-check-api)
- **Base URL:** `https://api-prd.kpn.com/network/kpn/disturbance-check`

#### Tags

- Network
- Broadband
- Service Assurance

#### Properties

- [Documentation](https://developer.kpn.com/products/kpn-disturbance-check-api)
- [Documentation](https://developer.kpn.com/documentation/kpn-disturbance-check-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/disturbance-check-kpn)
- [OpenAPI](openapi/kpn-disturbance-check-openapi.yml)

### KPN Internet Speed Check API

This API allows you to check the speed of the internet and the technology at an address. The API takes the postcode, house number and house extension, sends the request to the backend to retrieve real time information about the internet service at the address.

- **Human URL:** [https://developer.kpn.com/products/kpn-internet-speed-check-api](https://developer.kpn.com/products/kpn-internet-speed-check-api)
- **Base URL:** `https://api-prd.kpn.com/network/kpn/internet-speed-check`

#### Tags

- Network
- Broadband

#### Properties

- [Documentation](https://developer.kpn.com/products/kpn-internet-speed-check-api)
- [Documentation](https://developer.kpn.com/documentation/kpn-internet-speed-check-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/internet-speed-check-kpn)
- [OpenAPI](openapi/kpn-internet-speed-check-openapi.yml)

### KPN High Level Design FttX API

The High-Level Design FTTx API supports Fiber to the Home (FTTH) engineering jobs. It allows you to calculate the required work and cost for Fiber rollout in a provided region. Run the endpoints in this order: 1. **POST /startJobS3** to retrieve a signed URL for Amazon S3 bucket. Send this URL using the following endpoint. 2. **PUT /s3url_uploads/{jsonFileNameAndExtension}** to upload the job. 3. **GET /jobStatus/{jobId}** to retrieve the status of the job. 4. **GET / jobResultS3/{jobId}** to retrieve a signed URL for the Amazon Simple Storage Service (Amazon S3) bucket. Send this URL using the following endpoint. 5. **GET /Output/{jsonFileNameAndExtension}** to retrieve the results of the engineering job.

- **Human URL:** [https://developer.kpn.com/products/kpn-high-level-design-fttx-api](https://developer.kpn.com/products/kpn-high-level-design-fttx-api)
- **Base URL:** `https://api-prd.kpn.com/network/kpn/ftth-engineering/`

#### Tags

- Network
- Fiber
- FTTH
- Engineering

#### Properties

- [Documentation](https://developer.kpn.com/products/kpn-high-level-design-fttx-api)
- [Documentation](https://developer.kpn.com/documentation/kpn-high-level-design-fttx-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/high-level_design_ftth)
- [OpenAPI](openapi/kpn-high-level-design-ftth-openapi.yml)

### KPN LoRa Device Management API

KPN’s Low Power Long Range (LoRa) network service compliments existing 2G, 3G, 4G and LTE-M networks. It is based on the LoRaWAN protocol for Internet of Things (IoT).

- **Human URL:** [https://developer.kpn.com/products/kpn-lora-device-management-api](https://developer.kpn.com/products/kpn-lora-device-management-api)
- **Base URL:** `https://api-prd.kpn.com/data/lora/thingpark`

#### Tags

- IoT
- LoRaWAN
- Device Management

#### Properties

- [Documentation](https://developer.kpn.com/products/kpn-lora-device-management-api)
- [Documentation](https://developer.kpn.com/documentation/kpn-lora-device-management-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/lora-device-management-kpn)
- [OpenAPI](openapi/kpn-lora-device-management-openapi.yml)

### KPN SD-LAN / SD-WAN Network View API

The SD-LAN SD-WAN Network View API is a modern REST API based on the OpenAPI specification. The Network View API gives users read rights to retrieve information from the `Network View API` resources. - **Note**: By default you have read only access but based on your requirements and contract you can be granted `Manager` access to this API which is more than read only. To request manager access, please contact us at api_developer@kpn.com.

- **Human URL:** [https://developer.kpn.com/products/kpn-sd-lan-sd-wan-network-view-api](https://developer.kpn.com/products/kpn-sd-lan-sd-wan-network-view-api)
- **Base URL:** `https://api-prd.kpn.com/kpn/meraki`

#### Tags

- Network
- SD-WAN
- SD-LAN
- Enterprise Networking

#### Properties

- [Documentation](https://developer.kpn.com/products/kpn-sd-lan-sd-wan-network-view-api)
- [Documentation](https://developer.kpn.com/documentation/kpn-sd-lan-sd-wan-network-view-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/kpn-sd_lan_sd_wan_network_view_api)
- [OpenAPI](openapi/kpn-sd-lan-sd-wan-network-view-openapi.yml)

### KPN ServiceNow Connect API

This is Customer Connect API for KPN ServiceNow-Green Tickets. With this API KPN SN Green will be able to create new, or update existing tickets. This document provides the API specification.

- **Human URL:** [https://developer.kpn.com/products/kpn-servicenow-connect-api](https://developer.kpn.com/products/kpn-servicenow-connect-api)
- **Base URL:** `https://api-prd.kpn.com/network/kpn/servicenow`

#### Tags

- Service Management
- ITSM
- Ticketing
- OSS

#### Properties

- [Documentation](https://developer.kpn.com/products/kpn-servicenow-connect-api)
- [Documentation](https://developer.kpn.com/documentation/kpn-servicenow-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/servicenow-kpn)
- [OpenAPI](openapi/kpn-servicenow-connect-openapi.yml)

### KPN ISE API

Cisco Identity Services Engine (ISE) network access control resources exposed through the KPN API gateway, covering endpoints, endpoint groups, identity groups and internal users. The spec advertises a full-capability sandbox, HTTPS with OAuth, rate limiting and header-based versioning that defaults to the latest version.

- **Human URL:** [https://app.swaggerhub.com/apis-docs/kpn/ise-kpn](https://app.swaggerhub.com/apis-docs/kpn/ise-kpn)
- **Base URL:** `https://api-prd.kpn.com/kpn/ise`

#### Tags

- Network
- Security
- Identity Services Engine

#### Properties

- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/ise-kpn)
- [OpenAPI](openapi/kpn-ise-openapi.yml)

### KPN TV Guide API

This API provides you different TV related content services. Currently there are 3 main calls with some of them have successive calls. The data provided consists of JSON formatted text mainly related to TV content metadata. This data can be used to enrich all sort of platforms with actual TV data.

- **Human URL:** [https://app.swaggerhub.com/apis-docs/kpn/tv-guide-kpn](https://app.swaggerhub.com/apis-docs/kpn/tv-guide-kpn)
- **Base URL:** `https://api-prd.kpn.com/media/kpn/itv`

#### Tags

- Media
- TV
- EPG
- Content Metadata

#### Properties

- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/tv-guide-kpn)
- [OpenAPI](openapi/kpn-tv-guide-openapi.yml)

### KPN Webhook Signing Keys API

When KPN delivers a webhook to your endpoint, signing keys are to know the request genuinely came from KPN and wasn't tampered with in transit. KPN signs every outbound webhook payload using HMAC-SHA256 and includes the signature in a header. You store a shared secret on your side, compute the expected signature over the incoming request body, and compare it to the header value. If they match, the payload is genuine. This API lets you create and manage those shared secrets. **How signing keys work** You can set a signing key at three levels — Organization, Team, or Application. When KPN delivers a webhook, it picks the active key starting at the most specific level (Application), falling back to Team, then Organization. KPN automatically provisions an organization-level key on your first webhook delivery if you haven't created one. Each key moves through a simple lifecycle: -...

- **Human URL:** [https://app.swaggerhub.com/apis-docs/kpn/webhook-signing-key-management-kpn](https://app.swaggerhub.com/apis-docs/kpn/webhook-signing-key-management-kpn)
- **Base URL:** `https://api-prd.kpn.com/webhookconfigs-kpn`

#### Tags

- Webhooks
- Security
- Key Management

#### Properties

- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/webhook-signing-key-management-kpn)
- [OpenAPI](openapi/kpn-webhook-signing-keys-openapi.yml)

### KPN Webhook Privacy Config Manager API

KPN delivers outbound webhook notifications — such as SMS delivery reports — to the endpoints you configure. This API lets you control two things about those deliveries: the URL they are sent to, and which fields are included in the payload. **How configuration scopes work** You can configure webhooks at three levels — Organization, Team, or Application. Settings resolve from the most specific level to the broadest: an Application config overrides a Team config, which overrides the Organization config. This lets you set sensible defaults at org or team level and override them only where a specific application needs it. **Controlling payload fields (privacy)** `privacy_config.excluded_fields` maps a service name to the list of fields to omit from that service's outbound payloads. Any field not listed is included; an empty or absent map means every field is sent. Exclusion rules...

- **Human URL:** [https://app.swaggerhub.com/apis-docs/kpn/webhook-privacy-config-manager](https://app.swaggerhub.com/apis-docs/kpn/webhook-privacy-config-manager)
- **Base URL:** `https://api-prd.kpn.com/webhookconfigs-kpn`

#### Tags

- Webhooks
- Privacy
- Configuration

#### Properties

- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/webhook-privacy-config-manager)
- [OpenAPI](openapi/kpn-webhook-privacy-config-manager-openapi.yml)

### KPN Wholesale Broadband Access (WBA) API

KPN Wholesale Broadband Access (WBA) is a KPN Wholesale product offering copper and fiber access to wholesale customers. WBA has the following APIs available: * Functional Product Information: The Functional Product Information (FPI) service is used to provide WBA access information for new and existing WBA connections. FPI provides carrier vendor information and WBA technology availability with actual up and down bitrates with a reliability per technology type. * Carrier Information Product: information about the infrastructure and active services on the physical connection of a customer address.

- **Human URL:** [https://app.swaggerhub.com/apis-docs/kpn/wholesale-wba-kpn](https://app.swaggerhub.com/apis-docs/kpn/wholesale-wba-kpn)
- **Base URL:** `https://api-prd.kpn.com/wba/adresses`

#### Tags

- Wholesale
- Broadband
- Access

#### Properties

- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/wholesale-wba-kpn)
- [OpenAPI](openapi/kpn-wholesale-wba-openapi.yml)

### KPN Wholesale Broadband Access FPI/CIP API

KPN Wholesale Broadband Access (WBA) is a KPN Wholesale product offering copper and fiber access to wholesale customers. WBA has the following APIs available: * Functional Product Information: The Functional Product Information (FPI) service is used to provide WBA access information for new and existing WBA connections. FPI provides carrier vendor information and WBA technology availability with actual up and down bitrates with a reliability per technology type. * Carrier Information Product: The Carrier Information Product (CIP) service is used to provide information about the infrastructure and active services on the physical connection of a customer address.

- **Human URL:** [https://app.swaggerhub.com/apis-docs/kpn/wholesale-broadband_access_fpi_cip](https://app.swaggerhub.com/apis-docs/kpn/wholesale-broadband_access_fpi_cip)
- **Base URL:** `https://api-prd.kpn.com/wba`

#### Tags

- Wholesale
- Broadband
- Product Information

#### Properties

- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/wholesale-broadband_access_fpi_cip)
- [OpenAPI](openapi/kpn-wholesale-broadband-access-fpi-cip-openapi.yml)

### Polly.help Knowledge Management API

The Knowledge Management API allows you to organize your organization's information with knowledge management software.

- **Human URL:** [https://developer.kpn.com/products/pollyhelp-knowledge-management-api](https://developer.kpn.com/products/pollyhelp-knowledge-management-api)
- **Base URL:** `https://api-prd.kpn.com/data/pollyhelp/knowledgemanagement`

#### Tags

- Contact Center
- Knowledge Management
- Partner API

#### Properties

- [Documentation](https://developer.kpn.com/products/pollyhelp-knowledge-management-api)
- [Documentation](https://developer.kpn.com/documentation/pollyhelp-knowledge-management-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/knowledge-management-polly.help)
- [OpenAPI](openapi/pollyhelp-knowledge-management-openapi.yml)

### Xdroid Speech to Text API

Xdroid Speech To Text API provides a seamless audio transcription service.

- **Human URL:** [https://developer.kpn.com/products/xdroid-speech-text-api](https://developer.kpn.com/products/xdroid-speech-text-api)
- **Base URL:** `https://api-prd.kpn.com/data/kpn/voiceanalytics`

#### Tags

- Contact Center
- Speech to Text
- Voice Analytics
- Partner API

#### Properties

- [Documentation](https://developer.kpn.com/products/xdroid-speech-text-api)
- [Documentation](https://developer.kpn.com/documentation/xdroid-xdroid-speech-text-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/speech-to-text-xdroid)
- [OpenAPI](openapi/xdroid-speech-to-text-openapi.yml)

### Parley Secure Messenger API

This API enables a secure communication between your agent/bot desktop and the client website/mobile app.

- **Human URL:** [https://developer.kpn.com/products/parley-secure-messenger-api](https://developer.kpn.com/products/parley-secure-messenger-api)
- **Base URL:** `https://api-prd.kpn.com/communication/parley/secure-messenger`

#### Tags

- Messaging
- Chat
- Partner API

#### Properties

- [Documentation](https://developer.kpn.com/products/parley-secure-messenger-api)
- [Documentation](https://developer.kpn.com/documentation/parley-chat-and-messaging-api-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/secure-messenger-parley)
- [OpenAPI](openapi/parley-secure-messenger-openapi.yml)

### Tracebuzz Social Media Webcare API

The SocialMediaWebcare API allows you to organise and manage your inbound and outbound social media channels traffic.

- **Human URL:** [https://developer.kpn.com/products/social-media-chat-and-messaging](https://developer.kpn.com/products/social-media-chat-and-messaging)
- **Base URL:** `https://api-prd.kpn.com/communication/tracebuzz/social-media-webcare`

#### Tags

- Messaging
- Social Media
- Webcare
- Partner API

#### Properties

- [Documentation](https://developer.kpn.com/products/social-media-chat-and-messaging)
- [Documentation](https://developer.kpn.com/documentation/parley-webcare-parley-documentation-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/socialmediawebcare-tracebuzz)
- [OpenAPI](openapi/tracebuzz-social-media-webcare-openapi.yml)

### WeSeeDo Direct API

WeSeeDo Direct API allows you to set up a video communication channel between people by sending an SMS with a link to the meeting.

- **Human URL:** [https://developer.kpn.com/products/weseedo-weseedo-direct-api](https://developer.kpn.com/products/weseedo-weseedo-direct-api)
- **Base URL:** `https://api-prd.kpn.com/communication/weseedo/weseedodirect`

#### Tags

- Video
- Communications
- Partner API

#### Properties

- [Documentation](https://developer.kpn.com/products/weseedo-weseedo-direct-api)
- [Documentation](https://developer.kpn.com/documentation/weseedo-weseedo-direct-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/weseedo-direct-weseedo)
- [OpenAPI](openapi/weseedo-direct-openapi.yml)

### WeSeeDo Personal API

The WeSeeDo Personal API allows video calling in the right way and distinguishes itself in human contact, ease of use and safety.

- **Human URL:** [https://developer.kpn.com/products/weseedo-weseedo-personal-api](https://developer.kpn.com/products/weseedo-weseedo-personal-api)
- **Base URL:** `https://api-prd.kpn.com/communication/weseedo/weseedopersonal`

#### Tags

- Video
- Communications
- Partner API

#### Properties

- [Documentation](https://developer.kpn.com/products/weseedo-weseedo-personal-api)
- [Documentation](https://developer.kpn.com/documentation/weseedo-weseedo-personal-weseedo-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/weseedo-personal-weseedo)
- [OpenAPI](openapi/weseedo-personal-openapi.yml)

### Vonage Messages API (via KPN)

Encapsulates multiple APIs to interact with our various channels such as WhatsApp Business, SMS, MMS, Viber, Facebook Messenger, etc. The API normalises information across all channels to abstracted to, from and content. This API is for outbound messages.

- **Human URL:** [https://developer.kpn.com/products/vonage-messages-api](https://developer.kpn.com/products/vonage-messages-api)
- **Base URL:** `https://api-prd.kpn.com/communication/nexmo`

#### Tags

- Messaging
- CPaaS
- Resold API

#### Properties

- [Documentation](https://developer.kpn.com/products/vonage-messages-api)
- [Documentation](https://developer.kpn.com/documentation/vonage-messages-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/messages-nexmo)
- [OpenAPI](openapi/vonage-messages-openapi.yml)

### Vonage Voice API (via KPN)

The Voice API lets you create outboud calls, control in progress calls and get information about current and historical calls. The API is divided in 2 big resources blocks: - Application: Manage application level options - Call: Manage call level options ## Call Guidelines 1. Create an application 2. Make a call ## Guidelines to create an application In order to create an application, we need to provide 3 values: - name - type (voice) - answer_url - event_url For more information regarding the meaning of each field, refer to the <samp>POST /application</samp> endpoint. Among the return values of this call, there is the application identifier (<samp>uuid</samp>). It is needed to make calls or to operate with the application. ## Guidelines to make a call In order to make a call, we must include the identifier of the application in the **header** and fill the basic fields from the...

- **Human URL:** [https://developer.kpn.com/products/vonage-voice-api](https://developer.kpn.com/products/vonage-voice-api)
- **Base URL:** `https://api-prd.kpn.com/communication/nexmo/`

#### Tags

- Voice
- CPaaS
- Resold API

#### Properties

- [Documentation](https://developer.kpn.com/products/vonage-voice-api)
- [Documentation](https://developer.kpn.com/documentation/vonage-voice-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/voice-nexmo)
- [OpenAPI](openapi/vonage-voice-openapi.yml)

### Vonage Phone Numbers API (via KPN)

The Numbers API lets you manage your numbers and buy new virtual numbers for use with Vonage's APIs. ## Prerequirement: Your project has to be in the production environment in order to use of this API. For any questions, please contact our support team.

- **Human URL:** [https://developer.kpn.com/products/vonage-phone-numbers-api](https://developer.kpn.com/products/vonage-phone-numbers-api)
- **Base URL:** `https://api-prd.kpn.com/communication/nexmo/phone-numbers`

#### Tags

- Voice
- Phone Numbers
- CPaaS
- Resold API

#### Properties

- [Documentation](https://developer.kpn.com/products/vonage-phone-numbers-api)
- [Documentation](https://developer.kpn.com/documentation/vonage-phone-numbers-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/phone-numbers-nexmo)
- [OpenAPI](openapi/vonage-phone-numbers-openapi.yml)

### Vonage Number Insight API (via KPN)

Vonage's Number Insight API provides details about the validity, reachability and roaming status of a phone number, as well as giving you details on how to format the number properly in your application. There are three levels of the Number Insight API available: - Basic - Standard - Advanced The advanced API is available asynchronously as well as synchronously.

- **Human URL:** [https://developer.kpn.com/products/vonage-number-insight-api](https://developer.kpn.com/products/vonage-number-insight-api)
- **Base URL:** `https://api-prd.kpn.com/communication/nexmo/number-insight`

#### Tags

- Identity
- Number Insight
- CPaaS
- Resold API

#### Properties

- [Documentation](https://developer.kpn.com/products/vonage-number-insight-api)
- [Documentation](https://developer.kpn.com/documentation/vonage-number-insight-api-documentation)
- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/number-insight-nexmo)
- [OpenAPI](openapi/vonage-number-insight-openapi.yml)

### Vonage SMS API (via KPN)

Vonage's SMS API allows you to send and receive text messages to users around the globe through simple RESTful APIs. * Programmatically send and receive high volume of SMS anywhere in the world. * Build apps that scale with the web technologies that you are already using. * Send SMS with low latency and high delivery rates. * Receive SMS for free using SMS-enabled local numbers in countries around the world. * Only pay for what you use, nothing more.

- **Human URL:** [https://app.swaggerhub.com/apis-docs/kpn/sms-nexmo](https://app.swaggerhub.com/apis-docs/kpn/sms-nexmo)
- **Base URL:** `https://api-prd.kpn.com/communication/nexmo/sms`

#### Tags

- Messaging
- SMS
- CPaaS
- Resold API

#### Properties

- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/sms-nexmo)
- [OpenAPI](openapi/vonage-sms-openapi.yml)

### Vonage Verify API (via KPN)

Verify API is to Verify if a phone number is valid, reachable, and accessible by the user. Verification message can be customerized. Verify API provides the following services - **Verify Request** - Generate and send a PIN to your user. You use the request_id in the response is used for the Verify check. - **Verify Check** - Confirm that the PIN you received from your user matches the one sent by Vonage as a result of your Verify request. - **Verify Search** - Lookup the status of one or more requests. - **Verify Control** - Control the progress of your Verify requests.

- **Human URL:** [https://app.swaggerhub.com/apis-docs/kpn/verify-nexmo](https://app.swaggerhub.com/apis-docs/kpn/verify-nexmo)
- **Base URL:** `https://api-prd.kpn.com/communication/nexmo/verify`

#### Tags

- Identity
- Verification
- CPaaS
- Resold API

#### Properties

- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/verify-nexmo)
- [OpenAPI](openapi/vonage-verify-openapi.yml)

### Apidaze Voice CPaaS API (via KPN)

This REST API exposes actions that help your apps to interact with APIdaze’s Telco platform in mulitples ways. You can set the URL from where Apidaze fetchs XML instructions to run on Apidaze platform. You can write your various scripts there using the [Script Reference doc](https://developer.kpn.com/script-reference-documentation), and test them. You can manage your phone numbers, connect directly with other SIP carriers (inbound and outbound), manage your SIP accounts, voicemail boxes and messages, provision your hardphones.

- **Human URL:** [https://app.swaggerhub.com/apis-docs/kpn/apidaze-voice-voip-innovations](https://app.swaggerhub.com/apis-docs/kpn/apidaze-voice-voip-innovations)
- **Base URL:** `https://api-prd.kpn.com/communication/apidaze/cpaas`

#### Tags

- Voice
- VoIP
- CPaaS
- Resold API

#### Properties

- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/apidaze-voice-voip-innovations)
- [OpenAPI](openapi/apidaze-voice-openapi.yml)

### Registered Email API (via KPN)

This API offers three functionalities: - User management - Emailing User management can be used to add, get and modify user information. This can be done be a user with customer admin rights, without 2FA.Emailing can be used without authorization. The mail functionality can be used to sent registered emails with attachment without 2FA. Mail management, XML, can be seen by webservice users. It can be used to retrieve ticket information once the ticket id is known.

- **Human URL:** [https://app.swaggerhub.com/apis-docs/kpn/registeredemail-registeredemail](https://app.swaggerhub.com/apis-docs/kpn/registeredemail-registeredemail)
- **Base URL:** `https://api-prd.kpn.com/data/registeredemail/registeredemail`

#### Tags

- Email
- Registered Delivery
- Partner API

#### Properties

- [APIReference](https://app.swaggerhub.com/apis-docs/kpn/registeredemail-registeredemail)
- [OpenAPI](openapi/registered-email-openapi.yml)

### KPN GRIP API

KPN GRIP identity and access product. Documented on the KPN Developer portal; no public OpenAPI definition was found for this product on KPN's SwaggerHub organisation as of the harvest date.

- **Human URL:** [https://developer.kpn.com/products/kpn-grip-api](https://developer.kpn.com/products/kpn-grip-api)

#### Tags

- Security
- Identity
- Access Management

#### Properties

- [Documentation](https://developer.kpn.com/products/kpn-grip-api)
- [APIReference](https://developer.kpn.com/documentation/kpn-grip-api-documentation)

### KPN PIM ID API

KPN PIM app identity product. Documented on the KPN Developer portal; no public OpenAPI definition was found for this product on KPN's SwaggerHub organisation as of the harvest date.

- **Human URL:** [https://developer.kpn.com/products/kpn-pim-id-api](https://developer.kpn.com/products/kpn-pim-id-api)

#### Tags

- Identity
- Verification
- Mobile

#### Properties

- [Documentation](https://developer.kpn.com/products/kpn-pim-id-api)
- [APIReference](https://developer.kpn.com/documentation/kpn-pim-id-api-documentation)

### KPN SMS Campaigns API

Send and schedule bulk SMS campaigns over the KPN network. Documented on the KPN Developer portal; no public OpenAPI definition was found for this product on KPN's SwaggerHub organisation as of the harvest date.

- **Human URL:** [https://developer.kpn.com/products/sms-campaigns](https://developer.kpn.com/products/sms-campaigns)

#### Tags

- Messaging
- SMS
- Campaigns

#### Properties

- [Documentation](https://developer.kpn.com/products/sms-campaigns)
- [APIReference](https://developer.kpn.com/documentation/sms-campaign-documentation)

### KPN Email-to-SMS API

Converts inbound email into SMS messages delivered over the KPN network. Documented on the KPN Developer portal; no public OpenAPI definition was found for this product on KPN's SwaggerHub organisation as of the harvest date.

- **Human URL:** [https://developer.kpn.com/products/email-to-sms](https://developer.kpn.com/products/email-to-sms)

#### Tags

- Messaging
- SMS
- Email

#### Properties

- [Documentation](https://developer.kpn.com/products/email-to-sms)

## Common

- [Website](https://www.kpn.com/)
- [DeveloperPortal](https://developer.kpn.com/)
- [Documentation](https://developer.kpn.com/documentation)
- [GettingStarted](https://developer.kpn.com/page/getting-started)
- [SignUp](https://developer.kpn.com/dashboard/register)
- [Login](https://developer.kpn.com/dashboard/login)
- [Products](https://developer.kpn.com/products)
- [Tutorials](https://developer.kpn.com/tutorials)
- [Blog](https://developer.kpn.com/blog)
- [StatusPage](https://developer.kpn.com/status)
- [Support](https://developer.kpn.com/support)
- [TermsOfService](https://developer.kpn.com/page/legal)
- [VulnerabilityDisclosure](https://developer.kpn.com/page/responsible-disclosure)
- [OpenAPIRepository](https://app.swaggerhub.com/search?owner=kpn)
- [PostmanWorkspace](https://www.postman.com/kpndeveloper)
- [GitHubOrganization](https://github.com/kpn)
- [LinkedIn](https://www.linkedin.com/company/kpn)
- [Wholesale](https://www.kpn-wholesale.com/)
- [Standard](https://github.com/camaraproject/)
- [Standard](https://coin.nl/camara)

## Maintainers

- Kin Lane — kin@apievangelist.com
