# Transportation Management System for Microsoft Dynamics 365 Business Central

Help and Documentation of the [Shipper TMS on AppSource](https://marketplace.microsoft.com/en-us/product/dynamics-365-business-central/PUBID.extensionsforcelimited1647259189111%7CAID.tms-shippers%7CPAPPID.83e2e47e-de69-46f5-8e03-347521beda86?tab=Overview)

## Introduction

TMS is a comprehensive solution intended to streamline the transportation processes, including order management, scheduling, and tracking of shipments.

The Shipper TMS solution is ideal for scenario:
if you are a Shipper company that manages the transportation process of its sales, purchase and transfer orders and uses either its own transport with its drivers or hires, as well as uses third-party carriers [details](shipperscenario.md).


## Prerequisites

- Microsoft Dynamics 365 Business Central [product page](https://www.microsoft.com/en-us/dynamics-365/products/business-central). TMS is an add-on extension for Business Central that builds on its core modules—such as Customers, Sales, Vendors, Purchasing, and Warehousing—using them as a solid foundation while adding only the features necessary for transportation management.

## Installation

The TMS configuration process involves the creation and editing of TMS directories and entities to ensure optimal alignment of the TMS module with the company's business processes.

TMS comprises two main components: the core TMS and the Logistic Units extension. The core TMS utilizes functions provided by Logistic Units, which offers functionality for handling pallets and containers and features its own configuration system.

- Installation for Business Central On-line [See detailed instruction](installation.md)

## After Installation

After installing the TMS extension, several steps must be completed to make TMS available to users.

- Purchase and assign licenses. [See detailed instruction](buylicenses.md)
- Assign permission set to users [See detailed instruction](assignpermissionsets.md)

## How it works

Any document (sales, purchase, transfer orders) is passed to transportation by creating one or more Transport Requests.

- **Transport Request** : is a transportation request based on internal company documents, such as purchase orders, sales orders, or transfer orders. It defines **WHAT** : needs to be transported, where the goods are to be picked up, and where they need to be delivered, while also specifying the shipper and the consignee [details](transportrequest.md).

Based on the Transport Requests, the truck(s) for transportation are created — this is handled by the Transport Order.

- **Transport Order** : is a document that details **HOW** : the transportation will be carried out. It specifies the carrier, driver, and vehicle. The Transport Order represents the actual journey of the truck, outlining the stops where loading or unloading will take place [details](transportorder.md).

The relationship between Transport Requests and Transport Orders is many-to-many.
That is, one large order can be transported by multiple trucks (one Transport Request → many Transport Orders), and conversely, one truck can carry multiple orders (one Transport Order → many Transport Requests).

## Use cases

- Create Transport Request from Sales Order (Shipper) [details](usecase-salesorder-transportrequest.md).


## Tools
- **Load Management** Load Management is a tool designed for planning and scheduling cargo delivery. It allows users to allocate transportation requests to specific vehicles and routes, ensuring efficient delivery operations [deails](shipperloadmanagement.md).


## FAQ
[FAQ](faq.md) about TMS.

## Settings

### General

- **Transportation Conditions** Settings for managing different transportation conditions [details](transportationconditions.md)
- **Routes** - [details](route.md)
- **Route Sequence** -  [details](routesequence.md)
- **Compartments** - vehicle compartments control
- **Logistic Units Types** : is an item of any composition intended for transportation. Logistic units take many forms: a single box containing a limited number of products, a pallet with multiple products, or an intermodal container containing multiple pallets [details](logisticunittype.md).
- **Map Locations**. Map Locations is a directory of map-based locations utilized for precise pinpointing using geolocation services. Map Locations are employed for route mapping, distance calculations, and estimating transportation durations. Map Locations can be linked to the addresses of clients and suppliers. Useful if we have our own fleet [details](maplocation.md).
- **Map Location Types**. A directory of location types on the map, such as Client, Vendor, Port, Gateway, Hub, etc [details](maplocationtype.md).
- **Map Provider services** : integration. Configuration of Google Maps and TMS integration. It is needed for distance and duration estimation  [details](googlemapintegration.md)
- **Carriers**. A directory of third-party carriers that provide transportation services to our company [details](carrier.md).
- **Vehicles**. A directory of transportation vehicles, either owned by our company or by third-party carriers [details](vehicle.md).
- **Drivers**. Configuration of the directory for drivers, whether from our company or external [details](driver.md).
- **Routes**. Routes are used for the logical grouping of customer addresses by geographical attribute to facilitate the assignment of a set of customer orders to a specific truck or carrier [details](route.md).
- **Setup** : General settings of the TMS  [details](setup.md).

## Printing Forms, Documents, and Reports

[Available printing forms](reports.md)
