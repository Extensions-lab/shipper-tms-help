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

## Transport Orders

### When should we create a Transport Order directly?

Create it directly when you already know the trip structure and just need to attach requests and execute the load.

### Why can I not edit the Transport Order?

Most planning changes require the order to be in **Open** status.

### Why is **Carrier Selection** unavailable?

The order must be **Open**, and **Carrier Selection Enabled** must be turned on in **Shipper TMS Setup**.

## Planning pages

### Which planning page should I use?

Use:

- [Load Management](loadmanagement.md) for request-first planning
- [Truck Load Management](truckloadmanagement.md) for truck-first planning
- [Driver Load Management](driverloadmanagement.md) for driver-first planning
- [Visual Scheduler](visualscheduler.md) for timeline-based planning

### What is the difference between Truck Load Management and Driver Load Management?

Truck Load Management is centered on the vehicle slot. Driver Load Management is centered on the driver slot.

## Telematics

### Which telematics providers are supported?

Shipper TMS supports Geotab, Samsara, and Webfleet.

### Can different carriers use different providers?

Yes. Each carrier can point to its own **Telematics Setup Code**.

## Related

- [Installation](installation.md)
- [TMS Setup](setup.md)
- [Azure Maps integration](azuremapsintegration.md)
- [Transport Request](transportrequest.md)
- [Transport Order](transportorder.md)
