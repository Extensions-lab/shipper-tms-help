---
title: "Shipper TMS"
description: "User documentation for Shipper TMS, a transportation management extension for Microsoft Dynamics 365 Business Central."
---

# Shipper TMS for Microsoft Dynamics 365 Business Central

Shipper TMS helps manufacturers, distributors, and retailers plan and control their own deliveries without leaving Business Central.

Use it to:

- create transport demand from business documents,
- build loads and trips,
- assign carrier, vehicle, and driver,
- control capacity,
- print transport documents,
- connect telematics providers.

![Shipper TMS logo](resources/index/index-logo.png)

## Start here

If you are setting up the solution for the first time, follow this order:

1. [Install Shipper TMS](installation.md)
2. [Buy licenses](buylicenses.md)
3. [Assign permission sets](assignpermissionsets.md)
4. [Complete TMS Setup](setup.md)
5. [Create a Transport Request from a Sales Order](usecase-salesorder-transportrequest.md)
6. [Create your first Transport Order](usecase-create-first-transport-order.md)

## Core concepts

| Topic | What it explains |
|---|---|
| [Transport Request](transportrequest.md) | The planning document that captures what must be moved |
| [Transport Order](transportorder.md) | The execution document for the actual trip |
| [Products](product.md) | TMS product master data when your process uses it |
| [Statuses and Status Profiles](statuses.md) | Custom execution-status setup for controlled workflows |

## Planning tools

| Tool | Best for |
|---|---|
| [Load Management](loadmanagement.md) | Request-first planning |
| [Truck Load Management](truckloadmanagement.md) | Truck-first planning |
| [Driver Load Management](driverloadmanagement.md) | Driver-first planning |
| [Visual Scheduler](visualscheduler.md) | Timeline-based planning |
| [Carrier Selection](carrierselection.md) | Carrier comparison on a Transport Order |

## Setup and master data

| Topic | What it covers |
|---|---|
| [TMS Setup](setup.md) | Core system settings |
| [Carriers](carrier.md) | Transport service providers |
| [Vehicles](vehicle.md) | Fleet and capacity-driving vehicle records |
| [Drivers](driver.md) | Driver records and defaults |
| [Routes](route.md) | Geographic route grouping |
| [Route Sequence](routesequence.md) | Preferred stop order |
| [Map Locations](maplocation.md) | Geocoded stop records |
| [Map Location Types](maplocationtype.md) | Classification of map locations |
| [Zones](zones.md) | Internal zones and telematics geofences |
| [Time Slots and Delivery Schedules](timeslots.md) | Automatic date and time logic |
| [Transportation Conditions](transportationconditions.md) | Separation of incompatible cargo |
| [Logistic Unit Types](logisticunittype.md) | Capacity-related equipment profiles |
| [Map Providers](mapproviders.md) | Google Maps and Azure Maps setup |
| [Google Maps Integration](googlemapintegration.md) | Google-specific key setup |
| [Azure Maps Integration](azuremapsintegration.md) | Azure-specific account and key setup |

## Execution and integration

| Topic | What it covers |
|---|---|
| [Reports and Documents](reports.md) | Transport printouts and forms |
| [Telematics](telematics.md) | Geotab, Samsara, and Webfleet integration |

## Use cases

- [Use case: Create a Transport Request from a Sales Order](usecase-salesorder-transportrequest.md)
- [Use case: Create your first Transport Order](usecase-create-first-transport-order.md)

## FAQ

- [Frequently asked questions](faq.md)
