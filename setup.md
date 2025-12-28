---
title: "TMS Setup Guide"
description: "TMS Setup overview: status control, transport condition attribute, capacity checks (weight, volume, logistic units), auto-create transport requests, cost allocation defaults."
---

# Setup

On the TMS Setup page, the core settings for the TMS module are established, such as default types for created documents, document accounting features, numbering, etc.

## Where to find

TMS Setup is accessible via search

![Setup Image](resources/setup/pics/setup1.png)

or through Manual Setup in Advanced settings

![Setup Image](resources/setup/pics/setup2.png)

## Settings Description

![Setup Image](resources/setup/pics/setup3.png)

### General

- **Status Control**. Enabling/disabling the action control system for statuses across all profiles. Gloval control.
- **Transport Condition Attribute**. Transport Condition Attribute defines a product attribute that determines transportation conditions. For example, you can create a product attribute called “Transport Conditions” to be assigned to each item—or selected items—that require special handling (such as frozen or chilled goods), which cannot be transported together with regular items. Specifying transport conditions will result in order splitting and grouping based on these conditions.
You first need to create an Item Attribute and assign values to it.
For example:
Item Attribute = Transportation Conditions, Type = Option
Values = Frozen, Refrigerated, CRT, Ambient, Warm, Ventilation

### Control

This settings block defines the parameters controlled by the TMS. You can select the specific parameters that will be used as the basis for transportation planning.

- **Weight**. Specifies whether the system checks item weight capacity when placing or assigning orders.
- **Volume**. Specifies whether the system checks item volume capacity when placing or assigning orders.
- **Footage**. Specifies whether the system checks footage constraints before finalizing transport or freight orders.
- **Logistic Units**. Specifies whether the system checks the number of logistic units when assigning or finalizing an order.

Parameters that are not selected will not be displayed on pages or included in totals calculations.

### Transport Requests and Transport Order

 Shipper scenario-specific settings

- **Transport Request Nos.** : Specifies the number series code used for assigning numbers to transport requests by default.
- **Delivery Nos.** : Specifies the number series code used to assign numbers to carrier or Transport Orders.
- **Default Mode of Transport** : Specifies the default mode of transport used for new TMS deliveries or requests.
- **Default Charge Assignment Type** : Specifies the default charge assignment method for distributing carrier charges among deliveries or orders. This setting determines how transportation costs will be allocated to the orders that were shipped. For example, if we transported 10 orders using a third-party carrier who issued an invoice, we enter that invoice as a purchase invoice in Business Central. We then need to distribute the total amount of the carrier’s invoice across the transported orders. This can be done based on weight, amount, distance, or equally.
This setting defines the default allocation method, but it can be changed at any time in the cost allocation window within the Transport Order.
- **Default Item Charge Assignment Type** : Specifies the default item charge assignment method used when allocating costs within orders. This setting determines how transportation costs will be allocated to the item lines within an order—similar to the standard cost allocation functionality in Business Central. In other words, we distribute the portion of the transportation cost related to a specific order across the items included in that order.
This setting defines the default allocation method, but it can be changed at any time in the cost allocation window within the Transport Order.
- **Auto Create Transport Request for Sale** : Specifies whether a transport request is created automatically when a sales document is released.
- **Auto Create Transport Request for Purchase** : Specifies whether a transport request is created automatically when a purchase document is released.
- **Auto Create Transport Request for Transfer** : Specifies whether a transport request is created automatically when a transfer order is released.
- **Build Estimated Logistic Units** : Specifies whether the system builds logistic units automatically when creating new transport requests. For a preliminary estimate of how many logistics units (pallets, boxes) are needed, you can set up logistics unit formation rules—for example, how much of item X is required to form one pallet.
By defining these rules and enabling this setting, the system will estimate the number of pallets (or boxes, containers) required to transport the order when a Transport Request is created.
This helps in breaking down a large order into multiple shipments (i.e., multiple Transport Orders).
- **Delivery Execution Status Profile** : Specifies the status profile used to manage the execution steps of a Transport Order. This status profile is used to monitor the execution progress of a Transport Order, for example, via a Proof-of-Delivery app. Each line in the Transport Order has a status, and by updating it, you can effectively track the order fulfillment process.

## Additional Setup Functions

- **Set default reports** : Reset default reports settings (if you have problems with TMS reports). Path. "TMS Setup" > "Default Settings" > "Set default reports"
