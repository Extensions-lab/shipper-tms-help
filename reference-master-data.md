---
title: "Reference Master Data"
description: "Maintain supporting Shipper TMS reference data such as modes of transport, package types, fuel cards, IATA airports, and time zones."
---

# Reference Master Data

Use reference master data to keep planning fields consistent.

These records are usually maintained by an administrator or power user.

## Common reference tables

| Page | Use |
|---|---|
| **Mode of Transport** | Standard transport modes used on requests and orders |
| **Package Types** | Package classifications used by shipment and cargo details |
| **Fuel Cards** | Fuel-card master data for fleet operations |
| **IATA Airports** | Airport reference data for air-related routing or addresses |
| **Time Zones** | Time-zone reference values used by scheduling and route timing |

## Best practices

- Keep codes short and stable.
- Use business-readable descriptions.
- Do not create duplicate values with different spelling.
- Retire unused records only after checking open requests, orders, and integrations.

## Related

- [TMS Setup](setup.md)
- [Transport Request](transportrequest.md)
- [Transport Order](transportorder.md)
- [Visual Scheduler](visualscheduler.md)
