---
title: "Carriers"
description: "Set up carriers in Shipper TMS for default resources, rate comparison, scheduling, and telematics."
---

# Carriers

Use **Carriers** to define who executes transportation in Shipper TMS. A carrier can represent:

- your own fleet organization,
- an external transport company,
- or a subcontracted carrier you use for specific routes.

The carrier record is also where you connect default resources, carrier rates, and telematics.

## When to maintain a carrier

Create or update a carrier when you need to:

- assign a default vehicle or driver,
- compare carrier rates with **Carrier Selection**,
- connect a carrier to a telematics setup,
- filter planning by carrier,
- exclude a carrier from scheduling.

## How to work in this page

Use the carrier card to maintain the transport company and its default behavior.

1. Fill **General** and address/contact fields first.
2. If the carrier represents a Business Central vendor, employee, resource, or shipping agent, use **Source Type** and **Source No.** in **Link**.
3. In **Defaults**, set the default vehicle, driver, and vehicle unit type if they should be suggested on Transport Orders.
4. In **Route Points**, set start and end map locations if this carrier always starts or ends from fixed points.
5. In **Telematics**, set **Telematics Setup Code** if this carrier is connected to a provider.
6. In **Scheduler**, use **Scheduler Sort Order** to control display order and **Block for Scheduling** to hide the carrier from planning boards.
7. Use **Drivers** to review drivers linked to this carrier.
8. Use **Vehicles** to review vehicles linked to this carrier.
9. Use **Carrier Rates** when carrier selection is enabled and you maintain rates for this carrier.

## Create a carrier

1. Search for **Carriers**.
2. Open the list and choose **New**.
3. Fill in **No.** and **Name**.
4. Set **Mode of Transport** if you want it to default into new Transport Orders.
5. If needed, set:
   - **Default Vehicle No.**
   - **Default Driver No.**
   - **Default Unit Type**
6. If the carrier should use telematics, set **Telematics Setup Code**.
7. If the carrier should not appear in planning boards, enable **Block for Scheduling**.

## Fields that matter most in daily use

| Field | Why it matters |
|---|---|
| **Mode of Transport** | Helps default transport settings on new orders |
| **Default Vehicle No.** | Fills the vehicle automatically on a Transport Order |
| **Default Driver No.** | Fills the driver automatically on a Transport Order |
| **Default Unit Type** | Helps keep capacity and equipment consistent |
| **Telematics Setup Code** | Connects this carrier to a provider connection |
| **Blocked** | Prevents the carrier from being used in new work |
| **Block for Scheduling** | Removes the carrier from scheduler-based planning |

## What happens on a Transport Order

When you select a carrier on a Transport Order:

- the carrier name is filled,
- the default vehicle can be filled automatically,
- the default driver can be filled automatically,
- carrier-related telematics actions become available if the carrier has a telematics setup.

## Related

- [Carrier Selection](carrierselection.md)
- [Vehicles](vehicle.md)
- [Drivers](driver.md)
- [Telematics](telematics.md)
- [Transport Order](transportorder.md)
