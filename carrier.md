# Carrier

The Carrier entity is a comprehensive master data table in the Transportation Management System (TMS) that manages transportation service providers and their operational configurations.

It contains extensive carrier information including:

- basic identification (carrier number, primary and secondary names)
- Business Central integration (source type linking to vendors, resources, employees, or shipping agents with automatic name population)
- operational settings (freight agreement numbers, mode of transport, truckload shipping type, blocking status)
- default resource assignments (default vehicle, driver, and unit type with automatic name lookups)
- internet resources (website and tracking URLs)
- scheduling preferences (sort order and blocking controls)
- performance metrics (calculated fields for total distance, route quantity, and freight order counts).

The entity supports flexible integration with existing Business Central entities through an extensible source type enum, includes photo management capabilities, and features comprehensive card and list pages with navigation to related drivers, vehicles, and freight agreements.

The Carrier entity serves as the central hub for transportation service provider management within the TMS, enabling effective carrier selection, default resource assignment, performance tracking, and operational planning while supporting seamless integration with existing Business Central master data and providing detailed operational metrics for carrier evaluation and management.

## Fields Description

Basic Identification:

- **No.** : Carrier's unique identifier used in TMS freight operations
- **Name** : Primary name of the carrier for shipping references and TMS tasks
- **Name 2** : Second line for the carrier's name if additional details are needed

Business Central Integration:

- **Source Type** : BC entity type linked to this carrier (none, resource, vendor, employee, shipping agent)
- **Source No.** : Unique record ID from the chosen entity type for this carrier link
- **Source Name** : Name from the linked source entity (e.g., vendor name) used in TMS (auto-populated)
- **Source Name 2** : Additional line for the linked source name, if required (auto-populated)

Operational Configuration:

- **Freight Agreement No.** : Contract number for purchasing transportation services from this carrier
- **Mode of Transport** : Carrier's main transportation method, like road, sea, or air. This mode of transport will be automatically added to the document when the corresponding carrier is selected.
- **Blocked** : Indicates if this carrier is blocked and cannot be used for new shipments

Default Resource Assignments:

- **Default Vehicle No.** : Vehicle number automatically used on freight orders for this carrier. This vehicle will be automatically added to the document when the corresponding carrier is selected (if the Vehicle No. field in document was empty).
- **Default Vehicle Name** : Name of the default vehicle assigned to freight orders (auto-populated)
- **Default Driver No.** : Driver assigned by default to freight/delivery orders using this carrier. This driver will be automatically added to the document when the corresponding carrier is selected (if the Driver No. field in document was empty).
- **Default Driver Name** : Name of the default driver operating shipments (auto-populated)
- **Default Unit Type Code** : Default logistic unit type (e.g., container) for this carrier's shipments
- **Default Unit Type Description** : Details about the chosen logistic unit type (auto-populated)

Internet Resources:

- **Internet Address** : Carrier's website or online resource link for further information
- **Tracking Internet Address** : Link where shipments under this carrier can be tracked online

Shipping Configuration:

- **Truckload Shipping Type** : Whether this carrier typically handles full or partial truckloads

Scheduling Management:

- **Scheduler Sort Order** : Order in which this carrier is displayed in the scheduling tool (lower = higher priority)
- **Block for Scheduling** : Indicates if this carrier is prevented from appearing in scheduling due to maintenance or downtime

Visual and Media:

- **Picture** : Image or photo associated with this carrier (e.g. a logo)

Performance Metrics (Calculated Fields/ flowfields):

- **Total Actual Distance (Base)** : Sum of actual distances traveled for shipments under this carrier (calculated)
- **Total Route Quantity** : Total number of route entries in TMS for this carrier's shipments (calculated)
- **Freight Orders** : Number of freight orders linked to this carrier in TMS (calculated)

Obsolete Fields (Removed in v22.3):

- **Tracking Service Provider** : Obsolete tracking provider for shipments
- **Courier Code** : Obsolete code for the tracking service carrier

Audit Fields:

- **Last Modified Date Time** : When this record was last changed, for auditing or reference
- **Last Modified Date Time (UTC)** : Last modified timestamp in Coordinated Universal Time
- **Last Modified UserID** : User who made the most recent update to this carrier record
