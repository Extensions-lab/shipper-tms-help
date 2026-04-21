---
title: "Routes"
description: "Use routes to group transportation work by geography and to default resources in Shipper TMS."
---

# Routes

Use **Routes** to group customers, vendors, ship-to addresses, order addresses, and locations into logical transportation corridors.

A route in Shipper TMS is not a turn-by-turn map path. It is a planning label that helps you:

- group demand,
- filter requests,
- default carrier, vehicle, and driver values,
- plan by route in Visual Scheduler.

## How to work in this page

Use the route list when you maintain planning areas or recurring delivery corridors.

1. Add one row per logical route.
2. Use **Code** for a short route identifier that planners recognize.
3. Use **Description** to make the route understandable in filters and planning boards.
4. Set default carrier, vehicle, and driver only when that route normally uses the same resources.
5. Use **Scheduler Sort Order** to place common routes near the top of scheduler views.
6. Use **Block for Scheduling** when the route should not appear as a planning resource.
7. Drill down from **No. of Customers** when you want to review customers assigned to the route.

## Create a route

1. Search for **Routes**.
2. Add a new row.
3. Fill in **Code** and **Description**.
4. If needed, set:
   - **Default Carrier No.**
   - **Default Vehicle No.**
   - **Default Driver No.**
5. Set **Scheduler Sort Order** if you use route-based scheduling.
6. Enable **Block for Scheduling** only if the route should not appear in scheduler views.

## Assign a route to master data

Set **Default Route No.** on:

- **Customer**
- **Vendor**
- **Ship-to Address**
- **Order Address**
- **Location**

You can also set **Route Sequence** on the same records if the stop order usually follows a fixed sequence.

## How route defaults are used

Route values flow through the process like this:

1. The route is copied from master data to the source document.
2. The route is copied from the source document to the **Transport Request**.
3. If you set a route on a **Transport Order** and the carrier is still blank, the route's default carrier, vehicle, and driver can be applied.
4. When you run **Get Transport Requests**, the route can be used as a filter.

## Related

- [Route Sequence](routesequence.md)
- [Transport Request](transportrequest.md)
- [Transport Order](transportorder.md)
- [Visual Scheduler](visualscheduler.md)
