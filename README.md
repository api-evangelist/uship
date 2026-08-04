# uShip

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

uShip is an online shipping marketplace, founded in 2004 and headquartered in Austin, Texas, that connects
individuals and businesses with a network of professional transport service providers to move large, heavy, and
oversized freight — cars and light trucks, motorcycles and powersports, boats, furniture and household goods,
heavy equipment, and LTL freight. Shippers list a shipment for free and carriers compete with bids or bookable
published rates.

- Website: https://www.uship.com/
- Developer portal: https://developer.uship.com/ (invitation-only)
- Help center: https://help.uship.com/
- Status: https://uship.statuspage.io/
- GitHub: https://github.com/uShip

## APIs

The uShip API (v2) is a RESTful, hypermedia-driven JSON API over the marketplace, secured with OAuth 2.0
(`https://api.uship.com/v2`). Product surfaces documented on the developer portal include the core marketplace
API, Published Rates, LTL Connect, LTL Direct, Cars and Light Trucks, Furniture and Home Delivery, Integrator
Users, and Tracking.

**No machine-readable contract is published.** There is no OpenAPI/Swagger, AsyncAPI, GraphQL, MCP server, or
A2A agent card — the developer portal is invitation-only and `api.uship.com` answers every unauthenticated
request with `403 Missing Authentication Token`. Artifacts in this repo are captured from uShip's own published
documentation and live probes, never fabricated.

## Artifacts

| Directory | What it holds |
|---|---|
| `llms/` | uShip's published `llms.txt`, saved verbatim from https://www.uship.com/llms.txt |
| `authentication/` | The OAuth 2.0 profile — four grant types, token endpoints, required headers |
| `conventions/` | Hypermedia `links[]`, OData `$skip`/`$top` pagination, the value/label/shortLabel data trio, units, `testMode`, `checksum` |
| `errors/` | The `errors[]` envelope (errorCode/field/developerMessage/documentation/userMessage) |
| `asyncapi/` | The Published Rates webhook/callback surface (no AsyncAPI is published) |
| `sandbox/` | The `apistaging.uship.com` staging environment and the `testMode` flag |
| `lifecycle/` | Versioning, status page, API terms of use, and the absent deprecation/SLA posture |
| `conformance/` | Which standards the API does and does not conform to, with evidence |
| `data-model/` | The entity/relationship graph read from uShip's object reference |
| `packages/` | Registry sweep — no first-party SDK exists; two community npm wrappers |
| `well-known/` | The `/.well-known/` probe record (nothing published) |
| `security/` | Live TLS/HSTS/DNSSEC/CAA/SPF/DMARC probe results |
