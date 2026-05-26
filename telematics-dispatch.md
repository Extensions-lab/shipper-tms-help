---
title: "Telematics Dispatch"
description: "Publish, cancel, refresh, and review Shipper TMS Transport Order dispatches sent to telematics providers, including statuses, provider IDs, and results."
---

# Telematics Dispatch

Use telematics dispatch when a Transport Order should be sent to the provider as a route, job, or dispatch.

## Before you start

- The carrier has a telematics setup code.
- The telematics setup is enabled and has valid credentials.
- The Transport Order has route stops.
- Vehicle and driver mappings exist when the provider requires them.
- Dates, times, and addresses are complete enough for provider dispatch.

## Publish a Transport Order

1. Open the [Transport Order](transportorder.md).
2. Confirm the carrier, vehicle, driver, and route stops.
3. Choose **Publish to Telematics**.
4. Review the confirmation or provider result.
5. Open **Telematics Dispatches** to review the provider status.

Expected result:

- A telematics dispatch record is created or updated.
- The record stores provider, setup code, external dispatch ID, external status, vehicle and driver external IDs, stop count, and publish result.
- Provider-side route or dispatch data is available according to the provider's rules.

![Telematics dispatch log](resources/telematics/screenshot-telematics-dispatch-log.png)

## Cancel or refresh a dispatch

| Action | Use it when | Result |
|---|---|---|
| **Cancel Telematics Dispatch** | The dispatch should no longer be active in the provider | Sends a cancel request and updates the dispatch status |
| **Refresh from Telematics** | Provider status or stops may have changed | Reads provider data and updates local dispatch or execution facts |
| **Sync Execution Facts** | Execution entries need to be rebuilt from provider data | Creates or updates execution entries when the provider supplies facts |
| **Show Location** | Dispatcher needs current vehicle position | Opens current mapped vehicle location when available |

## Dispatch statuses and review fields

| Field | What it tells you |
|---|---|
| **Publication Status** | Local dispatch publication state |
| **External Dispatch ID** | Provider-side identifier |
| **External Status** | Latest provider-side status known to Shipper TMS |
| **Vehicle External ID** | Provider vehicle used for the dispatch |
| **Driver External ID** | Provider driver used for the dispatch |
| **Published At** | When publication succeeded |
| **Last Attempt At** | Last publish, refresh, or cancel attempt |
| **Last Result** | Latest provider result message |
| **Last Error Message** | Latest error text |
| **Reconciliation Needed** | Remote action succeeded but local projection still needs cleanup |

## Related

- [Telematics setup](telematics-setup.md)
- [Telematics provider mapping](telematics-provider-mapping.md)
- [Telematics sync and logs](telematics-sync-and-logs.md)
- [Transport Order](transportorder.md)
