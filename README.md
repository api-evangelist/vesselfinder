# VesselFinder (vesselfinder)

VesselFinder is a maritime intelligence company operating a global AIS vessel-tracking network (terrestrial AIS plus satellite AIS) and offering ship positions, voyage history, vessel particulars, port-call events, sea-distance routing, and ocean-container track-and-trace through its developer APIs. The platform pairs a credit-metered AIS REST API (Vessels, PortCalls, ExpectedArrivals, MasterData, Distance, plus subscription feeds VesselsList and LiveData) with a separate Container Tracking API that returns shipment schedules and real-time vessel positions by container number.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/vesselfinder/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - AIS, Maritime, Vessel Tracking, Container Tracking, Geospatial, Logistics, Ports, Supply Chain

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### VesselFinder AIS API

Credit-based and subscription REST API exposing the VesselFinder global AIS network. On-demand methods deduct credits per call; fleet- and area-wide feeds are subscription-priced. Authenticates via the `userkey` query parameter. Responses default to JSON; XML available via `format=xml`.

**Human URL:** [https://api.vesselfinder.com/docs/](https://api.vesselfinder.com/docs/)

- [Documentation](https://api.vesselfinder.com/docs/)
- [OpenAPI](openapi/vesselfinder-ais-api-openapi.yml)
- [JSON Schema — Vessel](json-schema/vesselfinder-vessel-schema.json)
- [JSON Schema — PortCall](json-schema/vesselfinder-port-call-schema.json)
- [JSON Structure — Vessel](json-structure/vesselfinder-vessel-structure.json)
- [JSON-LD Context](json-ld/vesselfinder-context.jsonld)
- [Naftiko Capability — Vessels](capabilities/ais-vessels.yaml)
- [Naftiko Capability — PortCalls](capabilities/ais-portcalls.yaml)
- [Naftiko Capability — ExpectedArrivals](capabilities/ais-expected-arrivals.yaml)
- [Naftiko Capability — MasterData](capabilities/ais-master-data.yaml)
- [Naftiko Capability — Distance](capabilities/ais-distance.yaml)
- [Naftiko Capability — VesselsList](capabilities/ais-vessels-list.yaml)
- [Naftiko Capability — LiveData](capabilities/ais-live-data.yaml)
- [Naftiko Capability — Status](capabilities/ais-status.yaml)

#### Methods

| Method | Purpose | Credits |
|---|---|---|
| `GET /vessels` | AIS position + optional Voyage / Master | 1 (TER) / 10 (SAT) + 1 voyage + 2 master |
| `GET /portcalls` | Arrival / departure events for vessel or port | 1–2 |
| `GET /expectedarrivals` | Vessels with announced ETA at a port | 5 AIS + 1 voyage + 2 master |
| `GET /masterdata` | Static vessel particulars by IMO | 3 |
| `GET /distance` | Shortest sea route between two coordinates | 1 |
| `GET /vesselslist` | Predefined fleet feed | Subscription |
| `GET /livedata` | Predefined area feed | Subscription |
| `GET /status` | Remaining credits + expiration date | 0 |
| `GET/POST/PUT/DELETE /listmanager` | Manage the fleet watchlist | 0 |

### VesselFinder Container Tracking API

Real-time ocean-container track-and-trace. Look up by 11-character container number + optional SCAC carrier (or `AUTO`). Returns origin, destination, schedule, transhipments, current vessel position, and progress. Asynchronous: 202 Accepted returned while data is fetched, poll at minimum 60 seconds.

**Human URL:** [https://container.vesselfinder.com/api/1.0/docs](https://container.vesselfinder.com/api/1.0/docs)

- [Documentation](https://container.vesselfinder.com/api/1.0/docs)
- [OpenAPI](openapi/vesselfinder-container-tracking-api-openapi.yml)
- [JSON Schema — ContainerShipment](json-schema/vesselfinder-container-shipment-schema.json)
- [Naftiko Capability — Containers](capabilities/container-tracking-containers.yaml)

## Pricing

| Pack | Units | Price |
|---|---|---|
| AIS Credits — 10,000 | 10k credits | €330 |
| AIS Credits — 20,000 | 20k credits | €625 |
| AIS Credits — 50,000 | 50k credits | €1,470 |
| Container Tracking — 1 | 1 container | $7 |
| Container Tracking — 10 | 10 containers | $65 |
| Container Tracking — 20 | 20 containers | $120 |
| Container Tracking — 50 | 50 containers | $275 |
| Container Tracking — 100 | 100 containers | $500 |
| VesselsList (Fleet) | Subscription | Quote |
| LiveData (Area) | Subscription | Quote |

Credits and container subscriptions expire 12 months after purchase. Container Tracking lookups are cached 12 hours; the same container is free to re-query within 30 days.

See also [plans/vesselfinder-plans-pricing.yml](plans/vesselfinder-plans-pricing.yml), [rate-limits/vesselfinder-rate-limits.yml](rate-limits/vesselfinder-rate-limits.yml), and [finops/vesselfinder-finops.yml](finops/vesselfinder-finops.yml).

## SDKs

- [VesselFinder AIS API Wrapper](https://github.com/VesselFinder/vesselfinder-api-wrapper) — PHP, Python
- [VesselFinder Container Tracking API Wrapper](https://github.com/VesselFinder/container-tracking-api-wrapper) — PHP, Python

## References

- [Flag Codes](https://api.vesselfinder.com/docs/flags.html)
- [AIS Ship Types](https://api.vesselfinder.com/docs/aistypes.html)
- [AIS NavStat](https://api.vesselfinder.com/docs/navstat.html)

## Examples

- [Vessels response](examples/vesselfinder-vessels-example.json)
- [PortCalls response](examples/vesselfinder-portcalls-example.json)
- [Distance response](examples/vesselfinder-distance-example.json)
- [Status response](examples/vesselfinder-status-example.json)
- [Container Tracking response](examples/vesselfinder-container-tracking-example.json)

## Tools

- [Web platform](https://www.vesselfinder.com)
- [Route Planner](https://route.vesselfinder.com)
- [VesselFinder for iOS](https://apps.apple.com/us/app/vesselfinder-lite/id918080862)
- [VesselFinder for Android](https://play.google.com/store/apps/details?id=com.astrapaging.vff)

## Maintainers

- **Kin Lane** — [API Evangelist](https://apievangelist.com)

## License

Profile content is published under API Evangelist terms. VesselFinder APIs are commercial — see [VesselFinder Terms of Use](https://www.vesselfinder.com/terms).
