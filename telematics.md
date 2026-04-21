---
title: "Telematics"
description: "Connect Shipper TMS to Geotab, Samsara, or Webfleet for dispatch publishing, tracking, route updates, and execution monitoring."
---

# Telematics

Use **Telematics** to connect Shipper TMS with external fleet systems.

The telematics integration lets you:

- publish Transport Orders to a provider,
- monitor execution from inside Business Central,
- view current and historical locations,
- bring back route changes,
- connect different carriers to different providers.

![Telematics Setup card with connection and sync actions](screenshot-telematics-setup-card.png)

## How to work in this setup window

Use **Telematics Setup** as the admin workspace for one provider connection.

1. Create one setup per provider account or tenant that should be used by Shipper TMS.
2. In **General**, select the provider and enable the setup.
3. In **Authentication**, enter the base URL, account values, and user name values required by the provider.
4. Choose **Manage Secrets** to store passwords, API keys, client secrets, refresh tokens, or webhook secrets.
5. Choose **Provider Parameters** when the provider needs extra values such as token URL, scope, region, API version, or webhook routing values.
6. Choose **Stream Setup** when you need to control sync mode, cadence, retry behavior, or webhook handling per stream.
7. Choose **Test Connection** before you run sync.
8. Turn on only the synchronization streams your company needs.
9. Run **Full Sync** for first setup, or run individual sync actions such as **Sync Vehicles**, **Sync Drivers**, **Sync Zones**, or **Sync Routes / Dispatches**.
10. Use **Entity Mappings** to verify how provider vehicles, drivers, and zones map to TMS records.
11. Use **Integration Log**, **Inbound Messages**, **Sync States**, and **Sync Locks** for troubleshooting.
12. Start **Background Polling** only after manual sync works.

After the setup works, open the [Carrier](carrier.md) card and assign the correct **Telematics Setup Code**.

## Supported providers

Shipper TMS currently supports:

- **Geotab**
- **Samsara**
- **Webfleet**

The data depth is not identical for every provider, but the operational setup pattern is consistent.

## Basic setup

1. Open **Shipper TMS Setup**.
2. Choose **Telematics Setups**.
3. Create a new setup.
4. Fill in the connection details for the provider.
5. Use **Manage Secrets** to store protected credentials.
6. Review **Provider Parameters** if the provider requires extra values.
7. Review **Stream Setup** if you want stream-level control.
8. Choose **Test Connection**.
9. Run **Full Sync** or only the sync actions you need.
10. On the [Carrier](carrier.md), set **Telematics Setup Code**.

## Common sync actions

Depending on the provider, you can run:

- **Sync Vehicles**
- **Sync Drivers**
- **Sync Zones**
- **Sync Routes / Dispatches**
- **Sync Trips**
- location and history sync actions

You can also enable **Background Polling Enabled** when you want automatic refresh.

## Publish a Transport Order

1. Open the **Transport Order**.
2. Make sure the carrier is connected to the correct telematics setup.
3. Prepare the vehicle, driver, and stop sequence.
4. Use the telematics publish action on the order.
5. Monitor the result in:
   - **Telematics Dispatches**
   - **Telematics Links**
   - integration log pages

## Bring external changes back

If the provider changes the route order or related execution data:

1. Refresh the telematics data for the setup or the order.
2. Use **Refresh from Telematics** on the Transport Order.
3. Review the returned changes before applying them.

## Zones and geofences

Telematics also works with [Zones](zones.md):

- internal zones can be mapped to provider zones,
- provider zones can be synchronized into snapshot tables,
- stop publication can use those mapped geofence references.

## Related

- [Transport Order](transportorder.md)
- [Carrier](carrier.md)
- [Zones](zones.md)
- [TMS Setup](setup.md)
