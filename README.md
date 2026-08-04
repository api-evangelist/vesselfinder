# VesselFinder (vesselfinder)

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
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

VesselFinder is a maritime intelligence company operating a global AIS vessel-tracking network
(terrestrial AIS plus satellite AIS) and offering ship positions, voyage history, vessel
particulars, port-call events, sea-distance routing, and ocean-container track-and-trace through
its developer APIs. The platform pairs a credit-metered AIS REST API (Vessels, PortCalls,
ExpectedArrivals, MasterData, Distance, plus subscription feeds VesselsList and LiveData) with a
separate Container Tracking API that returns shipment schedules and real-time vessel positions
by container number. VesselFinder also runs a public web map, iOS/Android apps, an embeddable
map widget, a fleet explorer, and a route planner.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/vesselfinder/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/vesselfinder/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- AIS
- Maritime
- Vessel Tracking
- Container Tracking
- Geospatial
- Logistics
- Ports
- Supply Chain

## Timestamps

- **Created:** 2026-05-25T00:00:00.000Z
- **Modified:** 2026-05-25

## APIs

### VesselFinder AIS API

Credit-based and subscription REST API exposing the VesselFinder global AIS network. On-demand
methods (Vessels, PortCalls, ExpectedArrivals, MasterData, Distance) deduct credits per call
proportional to dataset and source (terrestrial / satellite); fleet-wide (VesselsList) and
area-wide (LiveData) feeds are subscription-priced. Authenticates via the userkey query parameter.
Responses default to JSON and may be requested as XML.

- **Human URL:** [https://api.vesselfinder.com/docs/](https://api.vesselfinder.com/docs/)

#### Tags

- AIS
- Vessels
- Maritime
- Tracking

#### Properties

- [Documentation](https://api.vesselfinder.com/docs/)
- [Documentation](https://api.vesselfinder.com/docs/vessels.html)
- [Documentation](https://api.vesselfinder.com/docs/portcalls.html)
- [Documentation](https://api.vesselfinder.com/docs/expectedarrivals.html)
- [Documentation](https://api.vesselfinder.com/docs/masterdata.html)
- [Documentation](https://api.vesselfinder.com/docs/distance.html)
- [Documentation](https://api.vesselfinder.com/docs/vesselslist.html)
- [Documentation](https://api.vesselfinder.com/docs/livedata.html)
- [Documentation](https://api.vesselfinder.com/docs/status.html)
- [Documentation](https://api.vesselfinder.com/docs/listmanager.html)
- [OpenAPI](openapi/vesselfinder-ais-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/vesselfinder-ais-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vesselfinder-ais-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/vesselfinder-vessel-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Schema](json-schema/vesselfinder-port-call-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON Structure](json-structure/vesselfinder-vessel-structure.json)
- [JSON-LD](json-ld/vesselfinder-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### VesselFinder Container Tracking API

Real-time ocean-container track-and-trace API. Look up shipments by 11-character container
number and optional SCAC carrier code (AUTO to auto-detect). Returns origin, destination,
current vessel position, progress, and schedule events. Asynchronous: a first request may
return 202 Accepted while data is fetched; clients poll the same URL every 60 seconds or
more. Successful responses are cached for 12 hours and lookups for the same container
within 30 days are free.

- **Human URL:** [https://container.vesselfinder.com/api/1.0/docs](https://container.vesselfinder.com/api/1.0/docs)

#### Tags

- Container Tracking
- Logistics
- Supply Chain
- Maritime

#### Properties

- [Documentation](https://container.vesselfinder.com/api/1.0/docs)
- [Documentation](https://www.vesselfinder.com/container-tracking)
- [OpenAPI](openapi/vesselfinder-container-tracking-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/vesselfinder-container-tracking-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/vesselfinder-container-tracking-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/vesselfinder-container-shipment-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/vesselfinder-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

## Common Properties

- [Portal](https://www.vesselfinder.com)
- [Documentation](https://api.vesselfinder.com/docs/)
- [Documentation](https://container.vesselfinder.com/api/1.0/docs)
- [Getting Started](https://api.vesselfinder.com/docs/)
- [Pricing](https://www.vesselfinder.com/api)
- [Documentation](https://api.vesselfinder.com/docs/)
- [F A Q](https://api.vesselfinder.com/docs/)
- [Documentation](https://api.vesselfinder.com/docs/flags.html)
- [Documentation](https://api.vesselfinder.com/docs/aistypes.html)
- [Documentation](https://api.vesselfinder.com/docs/navstat.html)
- [Support](https://www.vesselfinder.com/contact)
- [Terms of Service](https://www.vesselfinder.com/terms)
- [Privacy Policy](https://www.vesselfinder.com/privacy)
- [Tool](https://route.vesselfinder.com)
- [Blog](https://www.vesselfinder.com/news)
- [Twitter](https://twitter.com/VesselFinder)
- [Facebook](https://www.facebook.com/vesselfinder)
- [YouTube](https://www.youtube.com/vesselfinder)
- [Application](https://apps.apple.com/us/app/vesselfinder-lite/id918080862)
- [Application](https://play.google.com/store/apps/details?id=com.astrapaging.vff)
- [GitHub Organization](https://github.com/VesselFinder)
- [SDK](https://github.com/VesselFinder/vesselfinder-api-wrapper)
- [SDK](https://github.com/VesselFinder/container-tracking-api-wrapper)
- [Plans](plans/vesselfinder-plans-pricing.yml)
- [Rate Limits](rate-limits/vesselfinder-rate-limits.yml)
- [Fin Ops](finops/vesselfinder-finops.yml)
- [Vocabulary](vocabulary/vesselfinder-vocabulary.yml)
- [Spectral Rules](rules/vesselfinder-rules.yml) — [Spectral](https://docs.stoplight.io/docs/spectral)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** info@apievangelist.com
**URL:** https://apievangelist.com
