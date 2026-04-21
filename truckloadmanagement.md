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

Do not start here if you only need to choose an external carrier. Use [Carrier Selection](carrierselection.md) on a Transport Order for that flow.

## Before you start

- Configure **Truck Load Time Slot Profile** in [TMS Setup](setup.md).
- Create vehicles and assign carrier, vehicle unit type, depot, capacity, and default driver when used.
- Create drivers if driver assignment is required before release.
- Transport Requests must be **Released** before they can appear as candidates.
- Capacity controls, compartments, and transportation conditions should be configured before go-live if your process enforces them.

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
   Shipper TMS creates an Open Transport Order for the selected truck slot.
6. In **Eligible Transport Requests**, select one or more requests.
7. Choose **Add to Selected Truck**.
   The requests are added to the slot's Transport Order if they pass eligibility checks.
8. Open the load with **Next Step**, **Load %**, or **Open Transport Order**.
9. When the load is ready, choose **Release Load**.
   The linked Transport Order changes from **Open** to **Released** when validation succeeds.

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

## Troubleshooting

| Problem | What to check |
|---|---|
| No truck slots are shown | Check planning period, time-slot profile, vehicle setup, carrier filter, vehicle unit type, depot filter, and whether the vehicle is blocked for scheduling. |
| Candidate requests are missing | Confirm requests are **Released**, inside the planning period, and compatible with the selected slot filters. |
| A candidate is blocked | Use **All With Reasons** or **Blocked Only** to see the reason. |
| **Add to Selected Truck** fails | The target slot and Transport Order must be selectable and open; capacity, compartment, and transportation-condition rules must allow the move. |
| **Release Load** fails | Resolve missing order, non-open order, missing requests, missing driver, conflict, overload, or compartment/condition blockers. |
| The linked order looks wrong | Use **Repair Truck Load Links** only when stale slot/order links must be rebuilt. |

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
