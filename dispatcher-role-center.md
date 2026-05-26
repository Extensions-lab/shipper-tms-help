---
title: "Dispatcher Role Center"
description: "Use the Shipper TMS Dispatcher Role Center to monitor daily planning cues, open operational lists, handle exceptions, and follow a dispatcher workflow."
---

# Dispatcher Role Center

Use the **Shipper TMS Dispatcher** Role Center when a dispatcher or transport planner needs one Business Central home page for the whole working day.

The Role Center brings together transport demand, active Transport Orders, same-day work, planning tools, telematics issues, and posted transport history.

## Who should use it

Use this Role Center for users who:

- plan released Transport Requests into loads,
- monitor Transport Orders that should depart or arrive today,
- react to overdue, late, overloaded, or incomplete assignments,
- work with Truck Load Management, Driver Load Management, Visual Scheduler, and Load Planning,
- review telematics issues and execution history.

## How to open it

Ask your Business Central administrator to assign the **Shipper TMS Dispatcher** profile to the dispatcher user.

After the profile is assigned, the user can open it from **My Settings** by selecting **Role Center** / **Role** depending on the Business Central version and client language.

The user also needs the relevant Shipper TMS permission set. If a cue or action is missing, check both the profile and permissions.

## What the headline tells you

The headline shows the most important dispatch state first. It is designed as a quick morning check before opening any worksheet.

Priority is:

| Headline priority | What it means |
|---|---|
| Critical overdue work | A Transport Order is overdue or should already have departed |
| Missing assignment | A released or active Transport Order is missing a required carrier, vehicle, or driver |
| Aged request | A Transport Request has waited longer than the configured aging threshold |
| Planning demand | Released Transport Requests are ready to be planned |
| Telematics issue | A dispatch, inbound message, or log entry needs attention |
| Warehouse document gap | A Warehouse Shipment or Warehouse Receipt still has no Transport Order |
| Daily status | No urgent exception is currently detected |

## Cue groups

The activities part is split into operational groups.

| Group | Cues | Use it for |
|---|---|---|
| **Transport Requests** | Open, Released, Assigned, Aged | Understand the request pool and find demand that has waited too long |
| **Transport Orders** | Open, Released, In Progress | Monitor trips by document status |
| **Today** | Departing Today, Arriving Today, Posted Today | Plan and track work for the current Business Central work date |
| **Dispatch Exceptions** | Overdue, Late Departures, Missing Assignments, Overloaded Loads, Telematics Issues, Warehouse Docs Without TO | Start with the work that needs intervention |

Choose a cue to open the filtered list behind it. For example, **Overdue** opens Transport Orders whose planned arrival is in the past and that are not posted.

## Main actions

The top navigation focuses on the pages a dispatcher opens often:

| Action | Use it when |
|---|---|
| **Transport Requests** | Review demand and release requests for planning |
| **Transport Orders** | Review, assign, release, execute, or post trips |
| **Visual Scheduler** | Work with a timeline view of requests and orders |
| **Truck Load Management** | Plan by vehicle, date, and time slot |
| **Customer Stop Pre-Planner** | Group released Transport Requests by customer stop before assigning a truck |
| **Driver Load Management** | Review driver workload and conflicts |
| **Load Planning** | Assign released requests to Transport Orders from a request-first worksheet |
| **Telematics Fleet Map** | Review fleet location when telematics is configured |

The creation actions let you create a new **Transport Request** or **Transport Order** directly from the Role Center.

## Menus

Use the menus when you need less frequent pages.

| Menu | What it contains |
|---|---|
| **Source Documents** | Sales Orders, Sales Return Orders, Purchase Orders, Purchase Return Orders, and Transfer Orders |
| **Master Data** | Carriers, rates, drivers, vehicles, products, routes, map locations, zones, time slots, statuses, IATA airports, and other transport reference data |
| **Telematics** | Fleet Map, dispatches, inbound messages, log entries, and telematics setup |
| **History** | Posted Transport Orders and Execution Entries |
| **Setup** | Shipper TMS setup and Logistic Units setup |

## Recommended daily workflow

1. Open the **Shipper TMS Dispatcher** Role Center.
2. Read the headline.
3. Clear **Dispatch Exceptions** first:
   - overdue Transport Orders,
   - late departures,
   - missing assignments,
   - overloaded loads,
   - telematics issues,
   - warehouse documents without Transport Orders.
4. Review **Today**:
   - orders departing today,
   - orders arriving today,
   - orders already posted today.
5. Plan the request pool:
   - open **Released** requests,
   - review **Aged** requests,
   - use **Load Planning**, **Truck Load Management**, **Driver Load Management**, or **Visual Scheduler**.
6. Open **Source Documents** when you need to create or review transport demand from sales, purchase, or transfer documents.
7. Release ready Transport Orders.
8. Monitor **In Progress** Transport Orders and telematics feedback.
9. Use **History** to review posted Transport Orders and execution entries after work is completed.

## Notes about dates

The same-day cues use the Business Central **Work Date**. If **Departing Today**, **Arriving Today**, or **Posted Today** does not match the calendar day you expect, check the user's work date.

## Troubleshooting

| Problem | What to check |
|---|---|
| The Role Center is not available | Confirm that the **Shipper TMS Dispatcher** profile exists and is assigned to the user |
| A cue is hidden or an action is missing | Check the user's Shipper TMS permission set and table permissions |
| Today cues look wrong | Check **Work Date** in Business Central |
| Missing Assignments is higher than expected | Review carrier, vehicle, driver, and setup rules for required driver assignment |
| Telematics Issues is empty but integration errors are expected | Check telematics setup, dispatches, inbound messages, log entries, and user permissions |

## Related

- [Transport Request](transportrequest.md)
- [Transport Order](transportorder.md)
- [Transport Request Load Planning](loadmanagement.md)
- [Truck Load Management](truckloadmanagement.md)
- [Driver Load Management](driverloadmanagement.md)
- [Visual Scheduler](visualscheduler.md)
- [Telematics](telematics.md)
- [Execution Entries](execution-entries.md)
- [Posted Transport Orders](posted-transport-orders.md)
