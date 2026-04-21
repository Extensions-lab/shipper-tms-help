---
title: "Telematics"
description: "Connect Shipper TMS to telematics providers such as Geotab, Samsara, and Webfleet."
---

# Telematics

Use **Telematics** when Shipper TMS must exchange route, dispatch, vehicle, driver, or execution data with a fleet platform.

Supported provider options include:

- **Geotab**,
- **Samsara**,
- **Webfleet**.

![Telematics Setup card with connection and sync actions](resources/telematics/telematics-setup-card.png)

## What telematics can support

Depending on provider setup, telematics can support:

- vehicle and driver mapping,
- route or dispatch publication,
- dispatch cancellation,
- vehicle location review,
- position history,
- route-stop events,
- execution fact synchronization,
- inbound messages and log review.

## Basic setup flow

1. Create a **Telematics Setup** record.
2. Select the provider.
3. Enter connection and authentication values.
4. Use provider-specific secret management where available.
5. Map vehicles and drivers.
6. Link the setup to the relevant [Carrier](carrier.md).
7. Test synchronization in a sandbox or demo company first.
8. Publish a test Transport Order.
9. Review telematics logs and inbound messages.

## Transport Order actions

A connected order can expose actions such as:

- **Publish to Telematics**,
- **Cancel Telematics Dispatch**,
- **Refresh from Telematics**,
- **Sync Execution Facts**,
- **Show Location**,
- **Telematics Dispatches**,
- **Telematics Links**.

The exact action result depends on the provider, credentials, mapping, and provider-side configuration.

## Telematics administration API

Shipper TMS also exposes API actions for telematics administration.

Examples include:

- registering or deleting a Samsara route webhook,
- ensuring or deleting a Webfleet route queue,
- retrieving a route-ingress contract,
- receiving provider webhook payloads.

For API entity sets and permission sets, see [API](api.md).

## Troubleshooting

| Problem | Check |
|---|---|
| Publish action fails | Provider credentials, carrier setup, route data, vehicle/driver mapping |
| No vehicle location appears | Vehicle mapping, provider sync status, last known position |
| Webhook is not received | API permissions, endpoint configuration, provider webhook registration |
| Execution entries are missing | Provider event availability, sync logs, status profile setup |

## Related

- [Carriers](carrier.md)
- [Vehicles](vehicle.md)
- [Drivers](driver.md)
- [Transport Order](transportorder.md)
- [Execution Entries](execution-entries.md)
- [API](api.md)
