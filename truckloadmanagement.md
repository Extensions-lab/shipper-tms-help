---
title: "Truck Load Management"
description: "Use Truck Load Management to plan by truck slot, review candidate requests, and release loads by vehicle, date, and time slot."
---

# Truck Load Management

Use **Truck Load Management** when your planner wants to work from the truck side first.

The main planning object is the **truck slot**:

- vehicle,
- planning date,
- time slot.

This page answers the question: **What should this truck carry in this time window?**

![Truck Load Management worksheet with truck slots and candidate requests](resources/truckloadmanagement/truck-load-management.png)

## When to use it

Use Truck Load Management when you want to:

- review all available trucks for a period,
- plan by resource instead of by request pool,
- see empty, full, overloaded, or conflicting truck slots,
- add requests directly to a selected truck,
- release a finished load.

## Main sections

| Section | Purpose |
|---|---|
| **Filters** | Period, carrier, vehicle unit type, time slot, depot, candidate mode |
| **Truck Slots** | One row per vehicle/date/time-slot combination |
| **Eligible Transport Requests** | Candidate requests for the currently selected slot |

## How to work in this window

1. Set the period with **Previous Period**, **Set Planning Period**, or **Next Period**.
2. Use **Carrier**, **Vehicle Unit Type**, **Time Slot**, and **Depot** filters as needed.
3. Select a truck slot in the upper list.
4. Review **Status**, **Next Step**, **Load %**, capacity columns, and conflicts.
5. If the slot has no Transport Order, choose **Create Load**.
6. In **Eligible Transport Requests**, select one or more requests.
7. Choose **Add to Selected Truck**.
8. Open the load with **Next Step**, **Load %**, or **Open Transport Order**.
9. When the load is ready, choose **Release Load**.

## Candidate modes

Use the **Candidates** filter to control how strict the lower list should be.

| Mode | Use it when |
|---|---|
| **Best Candidates** | You want the best planning suggestions first |
| **Eligible Only** | You want only requests that can be assigned |
| **All With Reasons** | You want to see why some requests are warnings or blocked |
| **Blocked Only** | You are troubleshooting planning blocks |

## Release checks

Before **Release Load** succeeds, Shipper TMS checks the selected truck slot.

Common blockers include:

- no linked Transport Order,
- Transport Order is not **Open**,
- no Transport Requests on the load,
- driver is required in setup but not assigned,
- slot has conflicts,
- load is overloaded,
- compartment or transportation-condition rules are not valid.

Fix the blocker, refresh the page, and release again.

## Move or remove work

1. Open the selected truck load from **Next Step**, **Load %**, or **Open Transport Order**.
2. Select the Transport Request row.
3. Choose **Remove from Truck** to return it to the planning pool.
4. Choose **Move to Another Truck** to move it to another truck slot.
5. Choose **Move to Another Driver** if the load should stay planned but change driver assignment.

## Main actions

| Action | Use it for |
|---|---|
| **Create Load** | Create an Open Transport Order for the current truck slot |
| **Show Selected Truck** | Refresh the candidate list for the current slot |
| **Add to Selected Truck** | Add selected requests to the selected slot |
| **Open Transport Order** | Open the linked Transport Order |
| **Release Load** | Release the current load after validation |
| **Repair Truck Load Links** | Repair stale slot/order links |

## Related

- [Driver Load Management](driverloadmanagement.md)
- [Load Management](loadmanagement.md)
- [Transport Order](transportorder.md)
- [Time Slots and Delivery Schedules](timeslots.md)
