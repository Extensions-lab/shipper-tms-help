---
title: "TMS Setup"
description: "Complete the core Shipper TMS setup for numbering, planning controls, map services, carrier selection, and execution."
---

# TMS Setup

Use **Shipper TMS Setup** to define the default behavior of Shipper TMS.

This page controls:

- number series,
- planning controls,
- automatic Transport Request creation,
- default transport values,
- carrier selection,
- freight-charge behavior,
- map providers,
- proof of delivery,
- telematics access.

![Main Shipper TMS Setup page](resources/setup/setup3.png)

## How to open the page

Use one of these options:

- search for **Shipper TMS Setup**,
- open it from **Manual Setup**,
- open the assisted setup flow if your company uses guided setup.

## Minimum setup checklist

Complete these items before planners start working:

1. Fill **Transport Request Nos.**
2. Fill **Transport Order Nos.**
3. Fill **MAP Location Nos.**
4. If you print CMRs, fill **CMR Nos.**
5. Set **Default Mode of Transport**.
6. Turn on the capacity controls your company uses:
   - **Weight**
   - **Volume**
   - **Footage**
   - **Logistic Units**
7. Set **Truck Load Time Slot Profile** if you use Truck Load Management or Driver Load Management.
8. Select the **Map Provider** and enter the required key.
9. Choose **Check TMS Settings**.

## Settings most teams use

| Area | What to review |
|---|---|
| **Number Series** | Transport Request, Transport Order, Map Location, and CMR numbering |
| **Control** | Capacity dimensions enforced during planning |
| **Transport Requests** | Automatic request creation from released sales, purchase, or transfer documents |
| **Transport Orders** | Default transport mode, charge assignment type, and driver requirement before truck-load release |
| **Transport Condition** | Item attributes used to separate incompatible cargo |
| **Carrier Selection** | Carrier comparison, rate-type mapping, and automatic charge-line creation |
| **Proof of Delivery** | PoD enablement and the transport execution status profile |
| **Map Provider Settings** | Google Maps or Azure Maps credentials |

## Recommended first-run sequence

1. Set the number series.
2. Select the capacity controls you will enforce.
3. Decide whether requests are created automatically when sales, purchase, or transfer documents are released.
4. Fill defaults such as **Default Mode of Transport**, **Truck Load Time Slot Profile**, and **Default Charge Assignment Type**.
5. Configure [Map Providers](mapproviders.md).
6. If you use Azure truck-aware routing, configure [Vehicle Routing Profiles](vehicle-routing-profiles.md).
7. If you use carrier comparison, configure [Carrier Rates](carrier-rates.md) and **Carrier Rate Types Mapping**.
8. If you use PoD or driver updates, configure [Statuses and Status Profiles](statuses.md).
9. If you use telematics, configure [Telematics](telematics.md).
10. Choose **Check TMS Settings**.

## Carrier selection settings

Use this section only when your company maintains carrier rates.

| Setting | Use |
|---|---|
| **Carrier Selection Enabled** | Shows Carrier Selection on Open Transport Orders |
| **Auto Create Charge Line** | Creates transport charge lines when a carrier is selected |
| **Carrier Rate Types Mapping** | Maps rate types such as rate, load, unload, return, and flat fee to charge behavior |

If carrier selection is enabled but rate-type mapping is missing, **Check TMS Settings** should be treated as a blocker before go-live.

## Useful actions

| Action | Use it for |
|---|---|
| **Check TMS Settings** | Validate whether the minimum required setup is complete |
| **Set default reports** | Restore the standard report selection setup |
| **Telematics Setups** | Open provider connections for Geotab, Samsara, or Webfleet |

## Verify setup

1. Search for **Transport Requests** and confirm the page opens.
2. Search for **Transport Orders** and confirm the page opens.
3. Create a test [Map Location](maplocation.md) and geocode it.
4. Create a test [Transport Request](transportrequest.md).
5. Create a test [Transport Order](transportorder.md).
6. Run **Get Transport Time & Distance** on the request or order.

## Related

- [Map Providers](mapproviders.md)
- [Vehicle Routing Profiles](vehicle-routing-profiles.md)
- [Carrier Rates](carrier-rates.md)
- [Carrier Selection](carrierselection.md)
- [Transport Charges](transport-charges.md)
- [Telematics](telematics.md)
