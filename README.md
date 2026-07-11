# FleetMon (fleetmon)

FleetMon was a Rostock, Germany based vessel tracking and maritime data provider (founded 2007) that operated one of the world's largest terrestrial AIS receiver networks alongside a documented REST API at `apiv2.fleetmon.com` covering vessel search, live and historical AIS positions, port calls, expected arrivals, next-port/ETA calculation, and voyage planning. Kpler acquired FleetMon alongside MarineTraffic in 2023; the FleetMon platform and API were phased out from January 2024 and migrated into MarineTraffic, and in September 2025 the combined AIS assets were unified under the **Kpler AIS** brand. As of 2026 the entire `fleetmon.com` domain — website, developer portal, and API host — no longer resolves.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/fleetmon/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/fleetmon/refs/heads/main/apis.yml)

## Access Model (Honest Status: RETIRED)

- **The FleetMon API is retired.** There is no live public API, no sign-up, and no developer portal. DNS for `fleetmon.com`, `www.fleetmon.com`, `developer.fleetmon.com`, `apidocs.fleetmon.com`, and `apiv2.fleetmon.com` returns no records.
- **Timeline:** Kpler announced the acquisition of MarineTraffic and FleetMon on February 15, 2023. FleetMon was phased out from January 2024, account logins were discontinued in February 2024, and the developer portal's final archived capture (January 2025) carries a notice that "the discontinuation of all FleetMon product offerings is imminent" with logins already disabled. On September 19, 2025 Kpler launched **Kpler AIS**, the unified successor to the MarineTraffic, FleetMon, and Spire Maritime AIS feeds.
- **What the API was:** a REST API (Swagger 2.0, final archived version 2.4.2) authenticated with an API key passed as an `apikey` query parameter, an `Api-Key` header, or an `Authorization: Token <apikey>` header. API access was sold on credit-based plans, and every response carried a `request_limit_info` block reporting consumption against your plan.
- **Where it went:** vessel tracking, AIS position, and port call data equivalents now live in the [MarineTraffic API portfolio](https://servicedocs.marinetraffic.com/) and [Kpler maritime data services](https://www.kpler.com/product/maritime/data-services), sold through Kpler sales rather than self-service FleetMon plans.
- **What this repository preserves:** the final publicly archived Swagger 2.0 definition of the FleetMon API, recovered from the Wayback Machine and annotated as retired, at [openapi/fleetmon-openapi.yml](openapi/fleetmon-openapi.yml). The endpoints in it are real, not modeled — and none of them are live.

## Tags

- Vessel Tracking
- Maritime
- AIS
- Ships
- Ports
- Port Calls
- Shipping
- Retired

## Timestamps

- **Created:** 2026-07-11
- **Modified:** 2026-07-11

## APIs

### FleetMon Vessels API (Retired)

Vessel master data surface — search the vessel database (`GET /vesselsearch/`), fetch basic and extended vessel particulars (`GET /basicvessel/{vessel_id}`, `GET /vessel/{vessel_id}`), vessel identity attributes, non-AIS vessel particulars, vessel photos, and manage tracked fleets (`GET/POST/PUT/DELETE /fleet/`).

- **Human URL (archived):** [http://web.archive.org/web/20250106234623/https://developer.fleetmon.com/reference/](http://web.archive.org/web/20250106234623/https://developer.fleetmon.com/reference/)
- **Base URL (retired):** `https://apiv2.fleetmon.com`

#### Properties

- [Archived API Reference](http://web.archive.org/web/20250106234623/https://developer.fleetmon.com/reference/)
- [OpenAPI (archived Swagger 2.0)](openapi/fleetmon-openapi.yml)

### FleetMon Vessel Positions API (Retired)

AIS position tracking surface — latest vessel position (`GET /vessel/{vessel_id}/position/`), fleet positions with extended vessel data (`GET /myfleet/`), historical AIS track reports (`GET /ais/position/`), historical AIS static and voyage messages (`GET /ais/static/`), dynamic AIS data, vessels inside a bounding box (`GET /regional_ais/`), and vessels near a position (`GET /vessel/near/`).

- **Human URL (archived):** [http://web.archive.org/web/20250106234623/https://developer.fleetmon.com/reference/](http://web.archive.org/web/20250106234623/https://developer.fleetmon.com/reference/)
- **Base URL (retired):** `https://apiv2.fleetmon.com`

#### Properties

- [Archived API Reference](http://web.archive.org/web/20250106234623/https://developer.fleetmon.com/reference/)
- [OpenAPI (archived Swagger 2.0)](openapi/fleetmon-openapi.yml)

### FleetMon Port Calls & ETA API (Retired)

Port intelligence surface — port search (`GET /portsearch/`), port calls per port and per vessel, vessels currently in port (`GET /port/inport/`), expected port arrivals (`GET /port/arrivals/`), next port and ETA calculation (`GET /vessel/{vessel_id}/ports/next/`), distance to port, voyage planning ETA and distance estimations (`POST /voyage-planning/`), and zone monitoring calls.

- **Human URL (archived):** [http://web.archive.org/web/20250106234623/https://developer.fleetmon.com/reference/](http://web.archive.org/web/20250106234623/https://developer.fleetmon.com/reference/)
- **Base URL (retired):** `https://apiv2.fleetmon.com`

#### Properties

- [Archived API Reference](http://web.archive.org/web/20250106234623/https://developer.fleetmon.com/reference/)
- [OpenAPI (archived Swagger 2.0)](openapi/fleetmon-openapi.yml)

## Common Properties

- [Website (Kpler, current owner)](https://www.kpler.com)
- [Legacy Website (offline)](https://www.fleetmon.com)
- [LinkedIn](https://www.linkedin.com/company/fleetmon-com)
- [Archived Developer Portal](http://web.archive.org/web/20250106234623/https://developer.fleetmon.com/)
- [Archived API Reference](http://web.archive.org/web/20250106234623/https://developer.fleetmon.com/reference/)
- [Acquisition Announcement (Kpler, Feb 2023)](https://www.kpler.com/blog/kpler-acquires-marinetraffic-and-fleetmon-for-maritime-sector-expansion)
- [Migration Guide (FleetMon → MarineTraffic)](https://support.marinetraffic.com/en/articles/9552991-fleetmon-and-marinetraffic-merge-process-for-former-fleetmon-ais-partners-from-january-2024)
- [Successor Announcement (Kpler AIS, Sep 2025)](https://support.marinetraffic.com/en/articles/12495052-19-september-2025-announcing-the-launch-of-kpler-ais)
- [Successor API Documentation (MarineTraffic API portfolio)](https://servicedocs.marinetraffic.com/)
- [Successor Product (Kpler maritime data services)](https://www.kpler.com/product/maritime/data-services)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
