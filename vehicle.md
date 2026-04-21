---
title: "Vehicles"
description: "Maintain vehicles in Shipper TMS for capacity checks, depot defaults, driver defaults, scheduling, and telematics."
---

# Vehicles

Use **Vehicles** to define the trucks, trailers, vans, and other equipment used in transportation planning.

The vehicle record affects:

- capacity control,
- default driver assignment,
- default depot handling,
- scheduling visibility,
- telematics mapping.

## How to work in this page

Use the vehicle card to keep planning capacity and resource assignment accurate.

1. Fill **General** with vehicle name, unit type, model, and depot.
2. In **Carrier**, select the carrier that owns or operates the vehicle.
3. In **Defaults**, set **Default Driver No.** if the same driver usually uses this vehicle.
4. Maintain registration and VIN values if you use compliance reporting or telematics matching.
5. Use **Fixed Asset** only if the vehicle should be linked to a Business Central fixed asset.
6. In **Scheduler**, set **Scheduler Sort Order** or **Block for Scheduling**.
7. If telematics is used, choose **Telematics Mapping** to link the vehicle to the external provider record.
8. Use **Show Location**, **Position History**, and **Telematics Log** only after the vehicle mapping exists.

## Create a vehicle

1. Search for **Vehicles**.
2. Choose **New**.
3. Fill in **No.**, **Name**, and **Carrier No.**.
4. Set **Unit Type Code**.
5. If needed, set **Default Driver No.**.
6. If the vehicle starts from a depot, set **Depot**.
7. If the vehicle should not appear in planning tools, enable **Block for Scheduling**.

## Why Unit Type matters

The most important field on the vehicle card is **Unit Type Code**.

That value defines the equipment profile used for:

- weight capacity,
- volume capacity,
- footage,
- logistic unit capacity,
- compartment setup when applicable.

Without the right unit type, capacity checks and truck-aware planning are much less reliable.

## Fields that matter most

| Field | Why it matters |
|---|---|
| **Carrier No.** | Ties the vehicle to the carrier that owns or operates it |
| **Unit Type Code** | Drives capacity and equipment behavior |
| **Default Driver No.** | Suggests a driver automatically |
| **Depot** | Can be used as the vehicle's default base location |
| **Registration No.** / **VIN No.** | Useful for telematics matching and compliance |
| **Block for Scheduling** | Hides the vehicle from scheduler-based planning |

## What happens on a Transport Order

When you assign a vehicle on a Transport Order:

- the vehicle name is filled,
- the vehicle type information can flow into the order,
- the default driver can be suggested,
- depot-related route behavior can be applied when configured.

## Related

- [Truck Load Management](truckloadmanagement.md)
- [Drivers](driver.md)
- [Carriers](carrier.md)
- [Logistic Unit Types](logisticunittype.md)
- [Transport Order](transportorder.md)
