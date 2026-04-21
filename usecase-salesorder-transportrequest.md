---
title: "Use Case: Sales Order to Transport Request"
description: "Create a released Transport Request from a released Sales Order in Shipper TMS."
---

# Use case: Create a Transport Request from a Sales Order

## Scenario

You have a Sales Order that must be handed over to transportation planning.

## Before you start

- The Sales Order must contain eligible item lines.
- The item lines must have **Location Code**.
- For an unposted Sales Order card, the document must be **Released** before **Create Transport Request** is available.

## Steps

1. Open **Sales Order**.
2. Create or review the item lines that need transportation.
3. Verify that each relevant line has **Location Code**.
4. Release the Sales Order.
5. Open the **Shipper TMS** action group.
6. Choose **Create Transport Request**.
7. Confirm the prompts shown by the system.
8. Open the created request if you want to review it immediately.

## Result

Shipper TMS creates a **Released Transport Request** for the remaining eligible lines of the Sales Order. The request stays linked to the source document and is ready for planning.

## Related

- [Transport Request](transportrequest.md)
- [Transport Order](transportorder.md)
- [Load Management](loadmanagement.md)
