# VesselFinder

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

VesselFinder is a maritime intelligence company operating a global AIS vessel-tracking network
(terrestrial AIS plus satellite AIS) and offering ship positions, voyage history, vessel
particulars, port-call events, sea-distance routing, and ocean-container track-and-trace through
its developer APIs. The platform pairs a credit-metered AIS REST API (Vessels, PortCalls,
ExpectedArrivals, MasterData, Distance, plus subscription feeds VesselsList and LiveData) with a
separate Container Tracking API that returns shipment schedules and real-time vessel positions
by container number. VesselFinder also runs a public web map, iOS/Android apps, an embeddable
map widget, a fleet explorer, and a route planner.

**Areas:** AIS · Maritime · Vessel Tracking · Container Tracking · Geospatial · Logistics · Ports · Supply Chain

## VesselFinder on APIs.io

Everything profiled for VesselFinder is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/vesselfinder/](https://apis.io/providers/vesselfinder/)** — or go straight to one of the APIs or properties below.

### APIs (10)

- [VesselFinder Containers API](https://apis.io/apis/vesselfinder/vesselfinder-containers-api/) — Real-time container track-and-trace.
- [VesselFinder Distance API](https://apis.io/apis/vesselfinder/vesselfinder-distance-api/) — Sea-route distance and geometry between two points.
- [VesselFinder Expected Arrivals API](https://apis.io/apis/vesselfinder/vesselfinder-expected-arrivals-api/) — Vessels with announced ETAs at a selected port.
- [VesselFinder List Manager API](https://apis.io/apis/vesselfinder/vesselfinder-list-manager-api/) — Manage the watchlist of vessels backing the VesselsList method.
- [VesselFinder Live Data API](https://apis.io/apis/vesselfinder/vesselfinder-live-data-api/) — All vessels within a predefined geographic area, subscription-based.
- [VesselFinder Master Data API](https://apis.io/apis/vesselfinder/vesselfinder-master-data-api/) — Static vessel particulars by IMO.
- [VesselFinder Port Calls API](https://apis.io/apis/vesselfinder/vesselfinder-port-calls-api/) — Arrival and departure events for vessels or ports.
- [VesselFinder Status API](https://apis.io/apis/vesselfinder/vesselfinder-status-api/) — Account status and remaining credits.
- [VesselFinder Vessels API](https://apis.io/apis/vesselfinder/vesselfinder-vessels-api/) — On-demand vessel position, voyage, and master data lookups.
- [VesselFinder Vessels List API](https://apis.io/apis/vesselfinder/vesselfinder-vessels-list-api/) — Predefined-fleet data, subscription-based.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Vesselfinder Agentic Access](https://apis.io/agentic-access/vesselfinder/vesselfinder-agentic-access/)

#### JSON Schema (3)

The data models the API reads and writes.

- [VesselFinder Container Shipment](https://apis.io/schemas/vesselfinder/vesselfinder-container-shipment/)
- [VesselFinder Port Call](https://apis.io/schemas/vesselfinder/vesselfinder-port-call/)
- [VesselFinder Vessel](https://apis.io/schemas/vesselfinder/vesselfinder-vessel/)

#### JSON Structure (1)

Data models expressed in JSON Structure.

- [Vesselfinder Vessel Structure](https://apis.io/json-structure/vesselfinder/vesselfinder-vessel-structure/)

#### JSON-LD (1)

Linked-data contexts for the provider's vocabulary.

- [Vesselfinder Context](https://apis.io/jsonld/vesselfinder/vesselfinder-context/)

#### Vocabulary (1)

The provider's domain terms, defined.

- [Vesselfinder Vocabulary](https://apis.io/vocabularies/vesselfinder/vesselfinder-vocabulary/)

#### Examples (3)

Example requests and responses.

- [Vesselfinder Container Tracking Example](https://apis.io/examples/vesselfinder/vesselfinder-container-tracking-example/)
- [Vesselfinder Distance Example](https://apis.io/examples/vesselfinder/vesselfinder-distance-example/)
- [Vesselfinder Status Example](https://apis.io/examples/vesselfinder/vesselfinder-status-example/)

#### Collections (22)

Postman and Open Collection request collections.

- [VesselFinder AIS API](https://apis.io/collections/vesselfinder/open-vesselfinder-ais-api/)
- [VesselFinder Container Tracking API](https://apis.io/collections/vesselfinder/open-vesselfinder-container-tracking-api/)
- [VesselFinder AIS Containers API](https://apis.io/collections/vesselfinder/open-vesselfinder-containers-api/)
- [VesselFinder AIS Containers Distance API](https://apis.io/collections/vesselfinder/open-vesselfinder-distance-api/)
- [VesselFinder AIS Containers Expected Arrivals API](https://apis.io/collections/vesselfinder/open-vesselfinder-expected-arrivals-api/)
- [VesselFinder AIS Containers List Manager API](https://apis.io/collections/vesselfinder/open-vesselfinder-list-manager-api/)
- [VesselFinder AIS Containers Live Data API](https://apis.io/collections/vesselfinder/open-vesselfinder-live-data-api/)
- [VesselFinder AIS Containers Master Data API](https://apis.io/collections/vesselfinder/open-vesselfinder-master-data-api/)
- [VesselFinder AIS Containers Port Calls API](https://apis.io/collections/vesselfinder/open-vesselfinder-port-calls-api/)
- [VesselFinder AIS Containers Status API](https://apis.io/collections/vesselfinder/open-vesselfinder-status-api/)
- [VesselFinder AIS Containers Vessels API](https://apis.io/collections/vesselfinder/open-vesselfinder-vessels-api/)
- [VesselFinder AIS Containers Vessels List API](https://apis.io/collections/vesselfinder/open-vesselfinder-vessels-list-api/)
- [VesselFinder AIS Containers API](https://apis.io/collections/vesselfinder/postman-vesselfinder-containers-api/)
- [VesselFinder AIS Containers Distance API](https://apis.io/collections/vesselfinder/postman-vesselfinder-distance-api/)
- [VesselFinder AIS Containers Expected Arrivals API](https://apis.io/collections/vesselfinder/postman-vesselfinder-expected-arrivals-api/)
- [VesselFinder AIS Containers List Manager API](https://apis.io/collections/vesselfinder/postman-vesselfinder-list-manager-api/)
- [VesselFinder AIS Containers Live Data API](https://apis.io/collections/vesselfinder/postman-vesselfinder-live-data-api/)
- [VesselFinder AIS Containers Master Data API](https://apis.io/collections/vesselfinder/postman-vesselfinder-master-data-api/)
- [VesselFinder AIS Containers Port Calls API](https://apis.io/collections/vesselfinder/postman-vesselfinder-port-calls-api/)
- [VesselFinder AIS Containers Status API](https://apis.io/collections/vesselfinder/postman-vesselfinder-status-api/)
- [VesselFinder AIS Containers Vessels API](https://apis.io/collections/vesselfinder/postman-vesselfinder-vessels-api/)
- [VesselFinder AIS Containers Vessels List API](https://apis.io/collections/vesselfinder/postman-vesselfinder-vessels-list-api/)

#### Governance rules (2)

Spectral rulesets for the provider's contracts.

- [VesselFinder — jsonschema rules](https://apis.io/rules/vesselfinder/vesselfinder-jsonschema-spectral-rules/)
- [VesselFinder API Rules](https://apis.io/rules/vesselfinder/vesselfinder-rules/)

#### Security (2)

Authentication, trust centre, and vulnerability disclosure.

- [Vesselfinder Authentication](https://apis.io/security/vesselfinder/vesselfinder-authentication/)
- [Vesselfinder Domain Security](https://apis.io/security/vesselfinder/vesselfinder-domain-security/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Vesselfinder Plans Pricing](https://apis.io/plans/vesselfinder/vesselfinder-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Vesselfinder Rate Limits](https://apis.io/rate-limits/vesselfinder/vesselfinder-rate-limits/)

#### FinOps (1)

What the API costs to run, by operation.

- [Vesselfinder Finops](https://apis.io/finops/vesselfinder/vesselfinder-finops/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.vesselfinder.com/)
- [Documentation](https://api.vesselfinder.com/docs/)
- [Getting started](https://api.vesselfinder.com/docs/)
- [Pricing](https://www.vesselfinder.com/api)
- [Support](https://www.vesselfinder.com/contact)
- [Blog](https://www.vesselfinder.com/news)
- [Terms of service](https://www.vesselfinder.com/terms)
- [Privacy policy](https://www.vesselfinder.com/privacy)
- [GitHub](https://github.com/VesselFinder)

## API Evangelist rating

**Kin Score 44.8** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 57.1 |
| Contract quality | 62.7 |
| Contract governance | 27.3 |
| Operational transparency | 5.3 |
| Developer ergonomics | 46.4 |
| Access clarity | 47.4 |

**Agent readiness 19.0** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | — |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | — |
| OpenAPI Examples | — |
| Rate Limit Signal | derived (partial credit) |
| Event Surface Described | — |
| Agent Skills | — |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | distinct |

**Regulatory alignment 24.5** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/vesselfinder/](https://apis.io/providers/vesselfinder/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for VesselFinder: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/vesselfinder/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
