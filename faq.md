---
title: "FAQ"
description: "Find quick answers to common installation, setup, planning, and execution questions for Shipper TMS."
---

# Frequently asked questions

## Installation and access

### Who needs a Shipper TMS license?

Only users who work directly with TMS features need a Shipper TMS license.

### Which permission set should a planner receive?

Most planners and dispatchers need **Shipper TMS - User**.

### Which permission set should an administrator receive?

Most administrators need **Shipper TMS - User** and **Shipper TMS - Administrator**.

## Setup

### What is the minimum setup before we start planning?

At minimum, fill in number series, default mode of transport, capacity controls, map provider settings, and truck-load time-slot profile if you use resource-first planning.

### Do we need a map provider?

No, but many route and distance features are much more useful when a map provider is configured.

### How do we set up Azure Maps?

Create an Azure Maps account in Azure, copy the **Primary Key** from **Authentication**, then enter it in **Shipper TMS Setup** as **Azure Maps Subscription Key**. See [Azure Maps integration](azuremapsintegration.md).

### When should we use transportation conditions?

Use them when incompatible goods such as frozen and ambient cargo must be kept separate.

## Transport Requests

### Why is **Create Transport Request** not available on a Sales Order?

For an unposted Sales Order card, the document must be **Released**, and the document must still contain eligible quantities that are not already assigned to a Transport Request.

### What is the difference between **Create Transport Request** and **Transport Request Planning**?

Use **Create Transport Request** for the normal one-step creation flow. Use **Transport Request Planning** when you need to split the document into multiple requests.

### Can one document create more than one Transport Request?

Yes. That is exactly what **Transport Request Planning** is for.

### Why can I not release a Transport Request?

The request must have **Load Date And Time** and **Unload Date And Time**.

### What changes when a Transport Request is assigned?

The request leaves the planning pool, shows as **Assigned**, and points to the linked Transport Order in **Assigned To**. To change the request freely again, remove it from the Transport Order first.

## Transport Orders

### When should we create a Transport Order directly?

Create it directly when you already know the trip structure and just need to attach requests and execute the load.

### Why is **Create Transport Order** unavailable on a source document?

If **Create Transport Requests Before Transport Orders** is turned off in **Shipper TMS Setup**, the source document must already have at least one **Released** Transport Request that is not assigned to another Transport Order. **Open** requests stay under user control and must be released manually.

If the setting is turned on, Shipper TMS can create missing Transport Requests first, creates them in **Released** status, releases existing **Open** Transport Requests, and then creates Transport Orders.

### Why can I not edit the Transport Order?

Most planning changes require the order to be in **Open** status.

### Why is **Carrier Selection** unavailable?

The order must be **Open**, and **Carrier Selection Enabled** must be turned on in **Shipper TMS Setup**.

### Why can I not post a Transport Order?

The order must be **In Progress**, must contain transport lines, and charge lines must be linked or posted correctly.

### Why can I not change a Transport Order?

Most planning changes require **Open** status. Reopen the order if it is **Released**.

### Why are warehouse documents not created?

The Transport Order must be **Released**, and the linked loading or unloading location must require warehouse shipment or receipt handling. Source lines must still have outstanding warehouse quantity.

## Planning pages

### Which planning page should I use?

Use:

- [Transport Request Load Planning](loadmanagement.md) for request-first planning
- [Truck Load Management](truckloadmanagement.md) for truck-first planning
- [Driver Load Management](driverloadmanagement.md) for driver-first planning
- [Visual Scheduler](visualscheduler.md) for timeline-based planning

### What is the difference between Truck Load Management and Driver Load Management?

Truck Load Management is centered on the vehicle slot. Driver Load Management is centered on the driver slot.

### Why does Truck Load Management show no candidates?

Check the planning period, slot filters, request status, route or depot filters, and whether the request is already assigned to a Transport Order.

### Why can I not release a truck load?

Common blockers are missing Transport Order, non-open Transport Order, no requests on the load, missing required driver, slot conflict, overload, or invalid compartment and transportation-condition rules.

## Carrier rates and charges

### Why does Carrier Selection show no carrier?

Check that the carrier is not blocked, rates match the route geography, map locations and distance data are usable, and rate-type mapping is complete when charge creation is expected.

### Does Carrier Selection use Region Code on Carrier Rates?

No. Carrier Selection currently matches rates by country/region code, county, city, and post code. **From Region Code** and **To Region Code** can be stored on the rate, but they are not used by the current matching logic.

### Why did Carrier Selection choose the carrier but not create charges?

Automatic charge creation requires **Auto Create Charge Line**, a vendor-based carrier, and rate type mappings with item charge numbers.

### Why did an API attachment upload fail?

Execution-entry attachments must be valid base64, 10 MB or smaller after decoding, and one of these MIME types: `image/jpeg`, `image/png`, `image/gif`, or `application/pdf`. The MIME type must match the actual file signature.

### Why does transport posting mention charge lines?

Posting checks whether charge lines are linked or whether linked sales, purchase, or transfer charge lines still need to be posted. Resolve the charge links before posting the Transport Order.

## Telematics

### Which telematics providers are supported?

Shipper TMS supports Geotab, Samsara, and Webfleet.

### Can different carriers use different providers?

Yes. Each carrier can point to its own **Telematics Setup Code**.

## Glossary

| Term | Meaning |
|---|---|
| Transport Request | Planning demand: what must be moved, from where, to where, and when. |
| Transport Order | Execution document for one trip, load, or delivery run. |
| Source document | Sales, purchase, transfer, or posted Business Central document that creates transport demand. |
| Carrier | External or internal transport service provider. |
| Vehicle | Truck, van, trailer, or other equipment used for transport. |
| Driver | Person assigned to execute or support a trip. |
| Map Location | Geocoded place used for route display, distance, and duration. |
| Logistic Unit Type | Capacity profile for pallets, containers, or other loading units. |
| Execution Entry | Status event, delivery update, attachment, picture, or proof-of-delivery fact. |
| Posted Transport Order | Read-only transport history after the Transport Order is posted. |

## Related

- [Installation](installation.md)
- [TMS Setup](setup.md)
- [Azure Maps integration](azuremapsintegration.md)
- [Transport Request](transportrequest.md)
- [Transport Order](transportorder.md)
