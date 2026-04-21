---
title: "Visual Scheduler"
description: "Use Visual Scheduler to review transportation demand on a timeline and adjust requests and orders visually."
---

# Visual Scheduler

Use **Visual Scheduler** when you want a timeline view of transportation work instead of a worksheet.

It is best for planners who want to see:

- when requests are planned,
- which requests are already grouped into orders,
- how the load changes over time,
- and where quick drag-and-drop adjustments are possible.

![Visual Scheduler timeline grouped by a planning dimension](resources/visualscheduler/screenshot-visual-scheduler.png)

## What the scheduler can show

The scheduler works with Transport Requests and the Transport Orders that group them.

Typical grouping options include:

- Carrier
- Driver
- Vehicle
- Route
- Consignee
- Shipper
- Transport Condition

## Main interactions

Depending on status and current context, planners can:

- move a request in time,
- resize a request to change the unload timing,
- drop a request into an Open Transport Order,
- open the related request or order,
- create a new Transport Order from selected requests.

## How to work in this window

Use this window when timing and visual grouping matter more than field-by-field planning.

1. Set the visible period with **Previous Period**, **Set Planning Period**, or **Next Period**.
2. Choose a **Group By** option:
   - **Carrier** when you review subcontractor or fleet workload,
   - **Driver** when you check driver workload,
   - **Vehicle** when you check equipment usage,
   - **Route** when you plan geographically,
   - **Consignee** or **Shipper** when you review demand by business partner,
   - **Transport Condition** when special handling matters.
3. Review unassigned Transport Requests and grouped Transport Orders on the timeline.
4. Drag an eligible request to change its timing.
5. Resize the request edge when you need to change the unload timing.
6. Drag a request into an **Open** Transport Order when it should travel with that order.
7. Double-click or use the context menu to open the related document.
8. Use multi-select and create a Transport Order when several eligible requests should become one trip.
9. Choose **Refresh** after changes made outside the scheduler.

If a request or order cannot be moved, check the document status. Released or In Progress orders are intentionally protected from visual rescheduling.

## When to use it

Use Visual Scheduler when you want to:

- spot gaps or overloads in the calendar,
- review work by route, vehicle, or driver,
- make quick timing adjustments,
- group eligible requests visually before creating the trip.

## Related

- [Load Management](loadmanagement.md)
- [Truck Load Management](truckloadmanagement.md)
- [Transport Request](transportrequest.md)
- [Transport Order](transportorder.md)
