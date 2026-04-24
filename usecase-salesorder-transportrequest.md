---
title: "Use Case: Sales Order to Transport Request"
description: "Create a released Transport Request from a released Sales Order in Shipper TMS."
---

# Use case: Create a Transport Request from a Sales Order

## Scenario

You have a Sales Order that must be handed over to transportation planning.

Use this process for a normal outbound customer delivery when the whole remaining eligible quantity can become transport demand.

## Before you start

- The Sales Order must contain eligible item lines.
- The item lines must have **Location Code**.
- For an unposted Sales Order card, the document must be **Released** before **Create Transport Request** is available.
- [TMS Setup](setup.md) must have **Transport Request Nos.** filled.
- Customer, ship-to, and location address data should be complete.
- Map locations should be configured if the planner needs distance, duration, or route display.

## Steps

1. Open **Sales Order**.
2. Create or review the item lines that need transportation.
3. Verify that each relevant line has **Location Code**.
4. Release the Sales Order.
   The **Create Transport Request** action becomes available if eligible quantities remain.
5. Open the **Shipper TMS** action group.
6. Choose **Create Transport Request**.
7. Confirm the prompts shown by the system.
8. Open the created request if you want to review it immediately.
9. Review shipper, consignee, load date/time, unload date/time, route, and request lines.
10. If the request is still **Open**, choose **Release** when it is ready for planning.

## Result

Shipper TMS creates a Transport Request for the remaining eligible lines of the Sales Order. The request stays linked to the source document.

The request is ready for planning when its status is **Released**. You can then assign it to a Transport Order from the request, from the Transport Requests list, or from a planning worksheet.

## What to do next

Choose one of these paths:

| Need | Next step |
|---|---|
| Add the request to a new trip immediately | Open **Transport Requests**, select the request, and choose **Create New Transport Order**. |
| Combine this request with other demand | Use [Transport Request Load Planning](loadmanagement.md) or [Visual Scheduler](visualscheduler.md). |
| Plan by own-fleet truck slot | Use [Truck Load Management](truckloadmanagement.md). |
| Select an external carrier later | Create or open the Transport Order, then use [Carrier Selection](carrierselection.md). |

## Troubleshooting

| Problem | What to check |
|---|---|
| **Create Transport Request** is unavailable | The Sales Order must be **Released** and must contain remaining eligible quantities. |
| No request is created | Check item lines, remaining quantities, location code, and whether the quantities were already assigned to another Transport Request. |
| The request cannot be released | Fill **Load Date And Time** and **Unload Date And Time** on the Transport Request. |
| The route is incomplete | Check customer, ship-to, location, and map location setup. |

## Related

- [Source Documents](source-documents.md)
- [Transport Request](transportrequest.md)
- [Transport Order](transportorder.md)
- [Transport Request Load Planning](loadmanagement.md)
