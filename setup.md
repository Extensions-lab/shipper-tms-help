---
title: "TMS Setup"
description: "Complete the core Shipper TMS setup for numbering, planning controls, map services, carrier selection, and execution."
---

# TMS Setup

Use **Shipper TMS Setup** to define the default behavior of the solution.

This page controls:

- number series,
- planning controls,
- default transport settings,
- carrier selection,
- map providers,
- proof of delivery,
- telematics access.

![Main Shipper TMS Setup page](resources/setup/pics/setup3.png)

## How to open the page

Use one of these options:

- search for **Shipper TMS Setup**,
- open it from **Manual Setup**,
- open the assisted setup flow if your company uses guided setup.

## Minimum setup checklist

Complete these items before planners start working in TMS:

1. Fill in **Transport Request Nos.**
2. Fill in **Transport Order Nos.**
3. Fill in **MAP Location Nos.**
4. If you print CMRs, fill in **CMR Nos.**
5. Set **Default Mode of Transport**
6. Turn on the capacity controls you need:
   - **Weight**
   - **Volume**
   - **Footage**
   - **Logistic Units**
7. Set **Truck Load Time Slot Profile** if you use Truck Load Management or Driver Load Management
8. Select the **Map Provider** and enter the required key

## Settings most teams use

| Area | What to review |
|---|---|
| **Control** | Which capacity dimensions should be enforced |
| **Transport Requests** | Auto-create settings and estimated logistic units |
| **Transport Orders** | Default transport mode, default charge behavior, driver requirement before release |
| **Transport Condition** | Item attribute used to separate incompatible cargo |
| **Carrier Selection** | Enable carrier comparison and optional auto charge creation |
| **Proof of Delivery** | Enable PoD and choose **Transport Execution Status Profile** |
| **Map Provider Settings** | Select Google Maps or Azure Maps and store credentials |

## How to work in this page

Use this page as an admin checklist, not as a daily dispatcher page.

1. Start with **Number Series** because Transport Requests, Transport Orders, Map Locations, and CMR documents need numbering before users work.
2. Go to **Control** and turn on only the dimensions your company really checks.
3. Go to **Transport Requests** and decide whether requests should be created automatically when sales, purchase, or transfer documents are released.
4. Go to **Transport Orders** and fill defaults such as **Default Mode of Transport**, **Truck Load Time Slot Profile**, and **Require Driver Before Release** if your process needs them.
5. Configure **Map Provider Settings** only after your map provider key is ready.
6. Use **Carrier Selection** settings only if you maintain carrier rates.
7. Use **Proof of Delivery** settings only if drivers or mobile users report execution statuses.
8. Choose **Check TMS Settings** after setup changes.
9. Choose **Set default reports** if print actions do not find the expected report layouts.
10. Choose **Telematics Setups** when you need to configure provider connections.

## Useful actions on the page

| Action | Use it for |
|---|---|
| **Check TMS Settings** | Validate whether the minimum required setup is complete |
| **Set default reports** | Restore the standard report selection setup |
| **Telematics Setups** | Open telematics provider connections |

## Recommended first-run sequence

After the minimum setup is complete:

1. Create at least one [Carrier](carrier.md)
2. Create at least one [Vehicle](vehicle.md)
3. Create at least one [Driver](driver.md) if your workflow requires drivers before release
4. Configure [Map Providers](mapproviders.md) if you want route maps and distance calculation
5. Create a test [Transport Request](transportrequest.md)
6. Create a test [Transport Order](transportorder.md)

## Related

- [Map Providers](mapproviders.md)
- [Azure Maps integration](azuremapsintegration.md)
- [Transportation Conditions](transportationconditions.md)
- [Time Slots and Delivery Schedules](timeslots.md)
- [Telematics](telematics.md)
- [Carrier Selection](carrierselection.md)
