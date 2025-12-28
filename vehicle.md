# Vehicle

The Vehicle entity is a comprehensive master data table in the Transportation Management System (TMS) that manages complete vehicle profiles for transportation operations.
It contains extensive vehicle information including:

- basic identification (vehicle number, name, type, model, manufacturer, year, color)
- technical specifications (VIN number, registration details
- engine specifications with type, number, power, and model)
- capacity and logistics data (unit type with internal dimensions and volume measurements)
- carrier and driver associations (linked carrier and default driver assignments)
- insurance coverage (main policy, CASCO, and VMTPLI policy numbers)
- fixed asset integration for financial tracking
- operational settings (scheduler preferences and blocking status)

The entity supports multiple vehicle types (car, truck, trailer, container) and engine types (diesel, petrol, electric, unknown) through extensible enums, includes photo management capabilities, and features comprehensive card and list pages for vehicle management.

The Vehicle entity serves as the central repository for fleet management within the TMS, enabling effective vehicle assignment, capacity planning, maintenance scheduling, compliance tracking, and operational management while supporting integration with financial systems through fixed asset linkage and providing detailed technical specifications for transportation planning and execution.

## Fields Description

Basic Identification:

- **No.** : Unique identifier for this vehicle, assigned from a number series or entered manually
- **Name** : Vehicle's name for easy recognition within TMS
- **Vehicle Type** : Category of this vehicle (car, truck, trailer, container) for classification within TMS

Unit Type and Capacity:

- **Unit Type Code** : Logistic unit type, outlining capacity and cargo parameters for this vehicle [details](logisticunittype.md)
- **Unit Type Description** : Describes the logistic unit type, clarifying the capacity details (auto-populated)
- **Unit Type - Linear UoM** : Measurement unit for the vehicle's linear dimensions (e.g., length) (auto-populated)
- **Unit Type - Internal Length** : Available internal length for cargo within this vehicle (auto-populated)
- **Unit Type - Internal Width** : Available internal width for cargo in this vehicle (auto-populated)
- **Unit Type - Internal Height** : Available internal height for cargo in this vehicle (auto-populated)
- **Unit Type - Internal Volume** : Total internal volume for cargo in this vehicle (auto-populated)
- **Unit Type - Volume** : Total volume capacity of this vehicle based on its unit type (auto-populated)
- **Unit Type - Volume UoM** : Unit of measure for this vehicle's volume capacity (auto-populated)

Carrier and Driver Association:

- **Carrier No.** : Carrier who owns or operates this vehicle (mandatory field) [details](carrier.md)
- **Carrier Name** : Name of the carrier that operates or owns this vehicle (auto-populated)
- **Default Driver No.** : Primary driver who is normally assigned to operate this vehicle [details](driver.md)
- **Default Driver Name** : Name of the primary driver assigned to operate this vehicle (auto-populated)

Location:

- **Def. Map Location** : Default map location for the vehicle's usual position, such as a parking area or depot. This location will be automatically added to the Delivery Order. This can be useful when the route is planned not from the loading point (warehouse), but from the truck's parking location, allowing for more accurate route and delivery time planning [details](maplocation.md).

Vehicle Identification:

- **VIN No.** : Vehicle identification number (VIN), a unique manufacturing code for this vehicle
- **Registration No.** : Official registration plate or number assigned to this vehicle
- **Registration Date** : Date on which this vehicle was officially registered

Engine Specifications:

- **Engine No.** : Unique engine serial number for this vehicle
- **Engine Power** : Vehicle's engine output, typically measured in horsepower or kilowatts
- **Engine Model** : Model of the vehicle's engine
- **Engine Type** : Engine category (diesel, gasoline, electric) of this vehicle

Vehicle Details:

- **Model** : Vehicle's model, used for reference in TMS
- **Manufacturer** : Company or brand that produced this vehicle
- **Year** : Manufacturing or model year of this vehicle
- **Color** : Primary color of this vehicle

Additional Information:

- **Comment** : Extra notes or observations about this vehicle. This comment is not copied to any TMS documents.

Insurance Coverage:

- **CASCO Insurance Policy No.** : CASCO policy, offering voluntary coverage for damages or theft of this vehicle
- **Insurance Policy No.** : Main insurance policy number covering this vehicle
- **VMTPLI No.** : VMTPLI policy, covering voluntary third-party liability in case of accidents

Fixed Asset Integration:

- **Fixed Asset No.** : Links this vehicle to a fixed asset record for financial or depreciation tracking
- **Fixed Asset Decription** : Describes the fixed asset record linked to this vehicle (auto-populated)

Operational Settings:

- **Scheduler Sort Order** : Position of this vehicle in scheduling, with lower values appearing first
- **Block for Scheduling** : Indicates if this vehicle is disallowed from scheduling for maintenance or unavailability

Visual and Media:

- **Picture** : Image or photo associated with this vehicle

Audit Trail:

- **Last Modified Date Time** : When this vehicle record was last updated
- **Last Modified Date Time (UTC)** : Last updated date/time in Coordinated Universal Time
- **Last Modified UserID** : User who last made changes to this vehicle record
