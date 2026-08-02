# uShip

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
