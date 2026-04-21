---
title: "Carrier Selection"
description: "Compare carrier rates for a Transport Order and apply the best carrier to the order."
---

# Carrier Selection

Use **Carrier Selection** on an **Open** Transport Order when you want Shipper TMS to compare carrier rates for the current route.

The feature helps planners choose a carrier based on configured pricing instead of manual estimates.

## How to work in this window

Use Carrier Selection after the route is planned enough to calculate costs.

1. Open the Transport Order.
2. Confirm that the order is **Open**.
3. Review the route stops and make sure addresses and distances are usable.
4. Choose **Carrier Selection**.
5. Review the carrier rows sorted by calculated cost.
6. Open or review the cost breakdown if you need to understand why a carrier costs more or less.
7. Select the carrier you want to use.
8. Confirm that **Carrier No.** and **Carrier Name** are updated on the Transport Order.
9. If **Auto Create Charge Line** is enabled, review the generated charge lines.

## Before you start

Make sure these items are in place:

1. **Carrier Selection Enabled** is turned on in [TMS Setup](setup.md)
2. carrier rates exist for the carriers you want to compare
3. route stops are already defined on the Transport Order
4. if you want automatic charges, enable **Auto Create Charge Line**

## Run Carrier Selection

1. Open the **Transport Order**.
2. Make sure the order status is **Open**.
3. Choose **Carrier Selection**.
4. Review the returned carrier list.
5. Select the carrier you want to apply.

## What the result includes

The comparison can include:

- route-based rate amount,
- flat fee amount,
- stop-related charges,
- return amount.

When you apply the result, the selected carrier is written back to the Transport Order.

If **Auto Create Charge Line** is enabled, Shipper TMS also creates charge lines on the order.

## If no good result appears

Check these items:

- the route has the stops you expect,
- the carrier is not blocked,
- the carrier has rates for the relevant route pattern,
- the pricing setup covers the countries, cities, or postal codes used by the route.

## Related

- [Carriers](carrier.md)
- [Transport Order](transportorder.md)
- [TMS Setup](setup.md)
