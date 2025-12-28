# Routes

The Route entity is a fundamental master data component within the Transportation Management System that serves as a geographic and operational grouping mechanism for organizing customers and optimizing delivery operations.

Routes enable logistics managers to define predefined paths or service areas that group customers geographically for efficient transportation planning and carrier assignment.

Each route contains essential operational information including a unique code identifier, descriptive text, and default resource assignments such as carrier, vehicle, and driver that are automatically applied when creating delivery orders or transport requests for customers assigned to that route.

The Route entity integrates deeply with the TMS workflow through automatic default assignments - when a customer is assigned to a route, the system automatically populates carrier, vehicle, and driver information in delivery orders and transport requests, streamlining the order creation process.
Routes also support scheduling functionality with a sort order field that determines the sequence in which routes appear in the TMS scheduler, and a blocking mechanism that can prevent routes from being included in scheduling activities.

The Routes page provides capabilities, displaying route information alongside a count of assigned customers with drill-down functionality to view the customer list. Routes are referenced throughout the TMS system in delivery orders, transport requests, and customer master data, making them essential for maintaining consistent transportation operations, optimizing resource utilization, and ensuring efficient geographic coverage across the transportation network.

## Fields Description

Primary Identification Fields:

- **Code** : Unique route code used to group customers geographically for TMS deliveries
- **Description** : Descriptive label for the route to help identify its coverage in TMS

Default Resource Assignment Fields:

- **Def. Carrier No.** : Default carrier assigned to shipments along this TMS route [about carrier](carrier.md)
- **Def. Vehicle No.** : Vehicle typically handling deliveries for this route [about vehicle](vehicle.md)
- **Def. Driver No.** : Driver commonly responsible for shipments on this route [about driver](driver.md)

Scheduling Control Fields:

- **Scheduler Sort Order** : Numerical order used to sort resources in the TMS scheduler
- **Block for Scheduling** : Whether this route is blocked from TMS scheduling activities

The table includes automatic validation logic in the "Def. Carrier No." field that cascades default vehicle and driver assignments from the carrier when a carrier is selected.

## Notes

The Route directory is used in the Shipper scenario of TMS.

## Use case

A typical route usage scenario. A default route is set for the customer, and this route is inherited by the created document (for example, a sales order). The route code is then passed on to the generated Transport Request.
The route code can then be used when selecting documents in the created Delivery Order (using the Get Documents function) or when creating a Delivery Order from a list of documents (e.g., sales orders) by filtering on the route field.
