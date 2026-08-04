# FleetMon (fleetmon)

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
