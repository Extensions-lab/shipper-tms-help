# Product

The Product entity is a comprehensive master data table within the Transportation Management System that defines and manages all products or items handled through TMS operations. This entity serves as the central repository for product information required for transportation planning, freight calculations, and logistics operations.

The Product table includes essential identification fields such as a unique code, description, and GTIN (Global Trade Item Number) for barcode and EDI integration, along with freight classification codes that determine shipping rates and handling requirements.

The entity features sophisticated weight and volume management capabilities, supporting both user-defined units of measure and automatic conversion to base units for standardized calculations across the system.

Products can have separate gross and net weight specifications, with automatic validation ensuring gross weight never falls below net weight.

The system also supports dimensional data (length, width, height) with automatic volume calculation, enabling accurate space planning and freight optimization. Volume and weight measurements can be specified in different units of measure while maintaining base unit conversions for consistent logistics calculations.

The Product List page provides an interface for managing all product data, displaying key information including identification codes, physical properties, freight classifications, and blocking status. The entity includes standard audit fields for tracking modifications and user accountability.

Products can be blocked from use in TMS operations, providing administrative control over product availability. This entity is essential for freight order processing, carrier selection, route optimization, and compliance with transportation regulations, serving as the foundation for accurate shipping calculations and logistics planning throughout the transportation management workflow.

## Fields Description

Primary Identification Fields:

- **Code** :  Unique product identifier for TMS shipments
- **Description** : Short product description for classification and handling
- **Unit of Measure Code** : How the product is measured (pieces, boxes, kg)
- **Freight Class** : Shipping classification for pricing and handling
- **GTIN** : Global Trade Item Number for barcodes and EDI documents

Weight Management Fields:

- **Weight Unit of Measure Code** : Weight unit (kg, lb) for mass measurement
- **Gross Weight** : Total weight including packaging
- **Net Weight** : Product weight excluding packaging materials
- **Gross Weight (base)** : Gross weight in base weight unit of measure
- **Net Weight (base)** : Net weight in base weight unit of measure

Volume Management Fields:

- **Volume Unit of Measure Code** : Volume unit (cubic meters) for measurement
- **Volume** : Total volume figure (length × width × height)
- **Volume (base)** : Volume in base volume unit of measure

Dimensional Fields:

- **Length** : Length of one item for freight/storage calculations
- **Width** : Width of one item for packing/loading
- **Height** : Height of one item for shipping/storage calculations

Control Fields:

- **Blocked** : Whether product is blocked from TMS operations

Audit Fields:

- **Last Modified Date Time** : Local timestamp of last modification
- **Last Modified Date Time (UTC)** : UTC timestamp of last modification
- **Last Modified UserID** : Username of last person to modify record

The table includes automatic validation ensuring gross weight never exceeds net weight, and automatic volume calculation when dimensional fields are updated.

## Notes

The Product directory is used in the LSP scenario of TMS when the Item directory is not used to describe the goods being transported in Forwarding Orders.

## Use Case

Product is used for a general description of the transported goods—for example, auto parts. We don’t need to specify exactly which parts, but it is necessary to include a cargo description in the documents.
