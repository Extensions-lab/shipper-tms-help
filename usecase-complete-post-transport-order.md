---
title: "Use Case: Complete and Post a Transport Order"
description: "Move a Transport Order through execution and post it to history."
---

# Use case: Complete and post a Transport Order

## Goal

Complete execution and move a live Transport Order to posted history.

## When to use it

Use this flow after route, carrier, vehicle, driver, warehouse, charges, and execution facts are ready.

## Before you start

- The Transport Order has route lines.
- Required charges are assigned or handled.
- Warehouse work is complete if your process requires it.
- Execution entries and PoD facts are reviewed if required.

## Steps

1. Open the Transport Order.
2. Confirm planning is complete.
3. Choose **In Progress** when execution starts.
4. Record execution entries or synchronize them from telematics.
5. Review charge assignments.
6. Resolve source document charge posting blockers.
7. Choose **Post**.
8. Open **Posted Transport Orders** and review the posted order.

## Expected result

- The live Transport Order is removed from the active order list.
- A Posted Transport Order is created.
- Posted lines, charges, assignments, and execution history are available for review.

## What to do next

Use posted history for audit, customer service, or delivery proof review.

## Common errors

| Problem | What to check |
|---|---|
| Post is unavailable | Order must be **In Progress** |
| Posting fails | Missing route lines, unassigned charges, unposted source charge lines, or required execution data |
| Posted order is not found | Confirm posting completed and search Posted Transport Orders |

## Related

- [Transport Order](transportorder.md)
- [Transport Charges](transport-charges.md)
- [Posted Transport Orders](posted-transport-orders.md)
