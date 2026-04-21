---
title: "Shipper TMS"
description: "User documentation for Shipper TMS, a transportation management extension for Microsoft Dynamics 365 Business Central."
---

# Shipper TMS for Microsoft Dynamics 365 Business Central

Shipper TMS helps manufacturers, distributors, and retailers plan and control their own deliveries in Business Central.

Use it to:

- create transport demand from sales, purchase, and transfer documents,
- build truck loads and trips,
- assign carriers, vehicles, and drivers,
- control capacity, compartments, and delivery windows,
- compare carrier rates and allocate freight cost,
- print transport documents,
- connect telematics providers,
- expose transport data through API pages.

![Shipper TMS logo](resources/index/index-logo.png)

## Start here

If you are setting up Shipper TMS for the first time, follow this order:

1. [Install Shipper TMS](installation.md)
2. [Buy licenses](buylicenses.md)
3. [Assign permission sets](assignpermissionsets.md)
4. [Complete TMS Setup](setup.md)
5. [Create a Transport Request from a Sales Order](usecase-salesorder-transportrequest.md)
6. [Create your first Transport Order](usecase-create-first-transport-order.md)

## Core concepts

| Topic | What it explains |
|---|---|
| [Source Documents](source-documents.md) | Where transport demand starts in sales, purchase, transfer, and posted documents |
| [Transport Request](transportrequest.md) | The planning document that captures what must be moved |
| [Transport Request Planning Worksheet](transport-request-planning.md) | How to split source lines across one or more requests |
| [Transport Order](transportorder.md) | The execution document for the actual trip |
| [Execution Entries](execution-entries.md) | Delivery, proof-of-delivery, and execution-status history |
| [Posted Transport Orders](posted-transport-orders.md) | Read-only history after a trip is posted |
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

## Cost and warehouse execution

| Topic | What it covers |
|---|---|
| [Carrier Rates](carrier-rates.md) | Rate setup used by Carrier Selection |
| [Transport Charges](transport-charges.md) | Purchase charges, sales re-billing, and charge allocation |
| [Warehouse Documents](warehouse-documents.md) | Warehouse shipments and receipts created from Transport Orders |
| [Reports and Documents](reports.md) | Loading Manifest, Packing List, Bill Of Lading, Delivery Note, and CMR Blank |

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
| [Vehicle Routing Profiles](vehicle-routing-profiles.md) | Azure Maps truck-routing constraints by unit type |
| [Distance Matrix](distance-matrix.md) | Stored distance and duration values |
| [Reference Master Data](reference-master-data.md) | Mode of transport, package types, fuel cards, IATA airports, and time zones |
| [Map Providers](mapproviders.md) | Google Maps and Azure Maps setup |
| [Google Maps Integration](googlemapintegration.md) | Google-specific key setup |
| [Azure Maps Integration](azuremapsintegration.md) | Azure-specific account and key setup |

## Integration

| Topic | What it covers |
|---|---|
| [Telematics](telematics.md) | Geotab, Samsara, and Webfleet integration |
| [API](api.md) | Business Central API pages exposed by Shipper TMS |

## Use cases

- [Use case: Create a Transport Request from a Sales Order](usecase-salesorder-transportrequest.md)
- [Use case: Create your first Transport Order](usecase-create-first-transport-order.md)

## Maintenance

- [Screenshot registry](screenshot-registry.md)
- [Frequently asked questions](faq.md)
