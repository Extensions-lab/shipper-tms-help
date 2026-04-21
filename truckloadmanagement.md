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

This page answers the question: "What should this truck carry in this time window?"

![Truck Load Management worksheet with truck slots and candidate requests](screenshot-truck-load-management.png)

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

Use this window from top to bottom.

1. Set the period with **Previous Period**, **Set Planning Period**, or **Next Period**.
2. Use **Carrier** when you plan one carrier at a time.
3. Use **Vehicle Unit Type** when you need only a specific equipment type, such as a truck, container, or trailer profile.
4. Use **Time Slot** when you plan a specific part of the day.
5. Use **Depot** when you want only trucks based at one depot.
6. Use **Candidates** to control the lower list:
   - choose the most restrictive mode when you only want suitable requests,
   - choose a mode that shows blocked requests when you need to understand why something cannot be loaded.
7. Select the truck slot in the upper list.
8. Review **Status**, **Next Step**, **Load %**, capacity columns, and conflicts.
9. If the slot has no Transport Order, choose **Create Load**.
10. In **Eligible Transport Requests**, select one or more requests.
11. Choose **Add to Selected Truck**.
12. Open the load with **Next Step**, **Load %**, or **Open Transport Order** to review the result.
13. When the load is ready, choose **Release Load**.

To remove or move work from a truck:

1. Open the selected truck load from **Next Step** or **Load %**.
2. Select the Transport Request row in **Selected Truck Load**.
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
| **Release Load** | Release the current load |
| **Repair Truck Load Links** | Repair stale slot/order links |

## Typical workflow

1. Open **Truck Load Management**.
2. Set the planning period and filters.
3. Select a truck slot.
4. Review the candidate list.
5. Choose **Create Load** if the slot does not yet have a Transport Order.
6. Select one or more candidate requests.
7. Choose **Add to Selected Truck**.
8. Review the load detail and then choose **Release Load** when ready.

## Status and next-step hints

The page shows status values such as:

- Empty
- Planned
- Partially Loaded
- Full
- Overloaded
- Released
- In Progress
- Unavailable
- Conflict

Use **Next Step** and **Load %** as quick indicators for where the planner should look next.

## Related

- [Driver Load Management](driverloadmanagement.md)
- [Load Management](loadmanagement.md)
- [Transport Order](transportorder.md)
- [Time Slots and Delivery Schedules](timeslots.md)
