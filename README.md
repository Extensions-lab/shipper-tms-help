# Transportation Management System for Microsoft Dynamics 365 Business Central

Help and Documentation of the [TMS on AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365-business-central/PUBID.extensionsforcelimited1647259189111%7CAID.tms%7CPAPPID.7bfc8c44-7cc8-4ba3-98d0-4f9964697a01?tab=Overview)

## Introduction

TMS is a comprehensive solution intended to streamline the transportation processes, including order management, scheduling, and tracking of shipments.

The TMS solution is ideal for two usage scenarios:

- if you are a Shipper company that manages the transportation process of its sales, purchase and transfer orders and uses either its own transport with its drivers or hires, as well as uses third-party carriers [details](shipperscenario.md).
- if you are a Logistic Service Provider (LSP) whose business involves the delivery of third-party goods, managing the transportation process and may also have its own fleet of vehicles and drivers or utilize services of third-party carriers. In this scenario, the mechanism for cost control and transparency in the invoicing process for transportation is crucial.

## Prerequisites

- Microsoft Dynamics 365 Business Central [product page](https://www.microsoft.com/en-us/dynamics-365/products/business-central). TMS is an add-on extension for Business Central that builds on its core modules—such as Customers, Sales, Vendors, Purchasing, and Warehousing—using them as a solid foundation while adding only the features necessary for transportation management.

## Installation and Setup

The TMS configuration process involves the creation and editing of TMS directories and entities to ensure optimal alignment of the TMS module with the company's business processes.

The configuration process is contingent on the company type, whether it is a Shipper, that is, it manages the shipment of its own goods, or an LSP (Logistic Service Provider), whose business revolves around managing the transportation of third-party cargo.

Many settings are utilized in both scenarios but with varying levels of detail.

TMS comprises two main components: the core TMS and the Logistic Units extension. The core TMS utilizes functions provided by Logistic Units, which offers functionality for handling pallets and containers and features its own configuration system.

- Installation for Business Central On-line [See detailed instruction](installation.md)

## After Installation

After installing the TMS extension, several steps must be completed to make TMS available to users.

- Purchase and assign licenses. [See detailed instruction](buylicenses.md)
- Assign permission set to users [See detailed instruction](assignpermissionsets.md)

## Settings

TMS supports two operation modes: Shipper and LSP. Some configurations and the documents used may vary significantly depending on the scenario.

### General

- **Setup** : General settings of the TMS  [details](setup.md).
- **Logistic Unit Type**. Templates for logistics units, such as pallets, containers, and boxes, define dimensional parameters: length, width, height, as well as fill control parameters: by weight or volume.
- **Map Locations**. Map Locations is a directory of map-based locations utilized for precise pinpointing using geolocation services. Map Locations are employed for route mapping, distance calculations, and estimating transportation durations. Map Locations can be linked to the addresses of clients and suppliers. Useful if we have our own fleet [details](maplocation.md).
- **Map Location Types**. A directory of location types on the map, such as Client, Vendor, Port, Gateway, Hub, etc [details](maplocationtype.md).
- **Map Provider services** : integration. Configuration of Google Maps and TMS integration. It is needed for distance and duration estimation  [details](googlemapintegration.md)
- **Carriers**. A directory of third-party carriers that provide transportation services to our company [details](carrier.md).
- **Vehicles**. A directory of transportation vehicles, either owned by our company or by third-party carriers [details](vehicle.md).
- **Drivers**. Configuration of the directory for drivers, whether from our company or external [details](driver.md).

### Shipper Scenario

If you are a Shipper company that manages the transportation process of its sales (and purchase) orders and uses either its own transport with its drivers or hires, as well as uses third-party carriers.

- **Transport Request** : is a transportation request based on internal company documents, such as purchase orders, sales orders, or transfer orders. It defines **WHAT** : needs to be transported, where the goods are to be picked up, and where they need to be delivered, while also specifying the shipper and the consignee [details](transportrequest.md).
- **Logistic Units Types** : is an item of any composition intended for transportation. Logistic units take many forms: a single box containing a limited number of products, a pallet with multiple products, or an intermodal container containing multiple pallets [details](logisticunittype.md).
- **Delivery Order** : is a document that details **HOW** : the transportation will be carried out. It specifies the carrier, driver, and vehicle. The Delivery Order represents the actual journey of the truck, outlining the stops where loading or unloading will take place [details](deliveryorder.md).
- **Routes**. Routes are used for the logical grouping of customer addresses by geographical attribute to facilitate the assignment of a set of customer orders to a specific truck or carrier [details](route.md).
- **Load Management** Load Management is a tool designed for planning and scheduling cargo delivery. It allows users to allocate transportation requests to specific vehicles and routes, ensuring efficient delivery operations [deails](shipperloadmanagement.md).

### Logistics Service Provider scenario (LSP)

If you are a Logistic Service Provider (LSP) whose business involves the delivery of third-party goods, managing the transportation process and may also have its own fleet of vehicles and drivers or use services of third-party carriers. In this scenario, the mechanism for cost control and transparency in the invoicing process for transportation is crucial.

- **Forwarding Order Types**. Templates for forwarding orders that establish the structure of the order and the business process for handling said order, as well as setting default values. Mandatory for LSP scenario [details](forwardingordertype.md).
- **Forwarding Order** : The central document in TMS for LSP, it is a request for transportation from either an external client or the company itself. It specifies **WHAT** : needs to be transported, where to pick up and deliver the item(s), identifies the shipper and consignee, outlines the logistic units being shipped, the relevant dates, and who will cover the costs, etc. [details](forwardingorder.md)
- **Logistic Units** : is an item of any composition intended for transportation. Logistic units take many forms: a single box containing a limited number of products, a pallet with multiple products, or an intermodal container containing multiple pallets.
- **Freight Order** : This document details **HOW** : the transportation will be executed, indicating who will actually carry it out. It specifies the carrier and the driver involved. The Freight Order reflects the actual journey of a truck or carrier [details](freightorder.md).
- **Settlement** : TMS supports a process of reconciling and finalizing all financial transactions associated with a particular service or operation [details](settlement.md).
- **Document Control** : A system for monitoring the availability of all required documents that are needed or may arise at different stages of the transportation management process [details](attachmentcontrol.md).
- **Stages profiles**. Defines the structure of the transportation process, including the number of stages, such as whether it will be a single-stage delivery or a three-stage multimodal transportation [details](stages.md).
- **Status profiles**. Statuses are used to organize the workflow of document processing in accordance with the business process. Different types of documents may have different status structures [details](statuses.md).
- **Services**. The Services directory is a reference within the TMS system designed for accounting for transportation services provided by the company. These services are used to invoice clients for transportation services. Required for invoicing [details](services.md).
- **Charges**. The Charges directory is a reference within the TMS system intended for the recording and allocation of costs to orders and the calculation of profitability for transportation orders. Required for profit calculation [details](charges.md).
- **Service Set**. This setting allows for the definition of sets of services and costs that can be added automatically when creating orders, or for the use of restrictions on the sets of services and costs that can be utilized in an order.
- **Content Set**. Predefined set of content automatically added to an order upon its creation.
- **Freight Order Types**. Templates for freight orders define order parameters, including the status structure and the model for order numbering.
- **Freight Classes**. The Freight Class Directory is a standardized classification system for less-than-container load (LCL) freight shipments, categorizing them based on specific attributes. The classification of cargo freight is established using various criteria, such as value, weight, length, density, and additional factors.

## Use cases

### Delivery of a simple sales order. Selling own goods. Delivery using own transport

Shipper scenario. In this case, the sequence of steps is as follows:

Steps:

1. A [Transport Request](transportrequest.md) is created for the sales order—either manually from the sales order card or automatically when the document is released. This way, the document is handed over for transportation.
2. The [Transport Request](transportrequest.md) is then added to a new or existing [Delivery Order](deliveryorder.md) by selecting it directly in the Delivery Order document via Prepare → Get Transport Requests, or by using the Load Management tool.
3. Define Vehicle and Driver in Delivery order.

### Customer’s international freight order. Transport the cargo. Collect the costs. Invoice the customer. Using third-party carriers

LSP scenario. Use the combination of [Forwarding Orders](forwardingorder.md) and [Freight Orders](freightorder.md).

Settings: Create a Forwarding Order Type with:

- A stage structure reflecting the actual transportation (e.g., pickup → main carriage by sea → delivery to consignee).
- A status profile aligned with the company’s order handling process.

Steps:

1. Create a Forwarding Order.
2. Assign the appropriate Forwarding Order Type.
3. Enter the Ordering Party (the customer who ordered the transport and will be invoiced).
4. Fill in the Shipper and Consignee details.
5. Add order lines, specifying the cargo to be transported. (Optional) Enter planned pickup and delivery dates.
6. For each stage of the Forwarding Order, create a Freight Order (who will actually do this transportation leg).
7. In Settlement, record costs by linking supplier invoices related to this shipment (e.g., invoices from carriers).
8. In Settlement, add Income lines for the services to be billed to the Ordering Party.
9. Issue the customer invoice.
10. Post related documents in settlement (sales and purchase documents) and post the Forwarding Order.
