---
title: "Carrier Selection"
description: "Compare carrier rates for a Transport Order and apply the best carrier to the order."
---

# Carrier Selection

Use **Carrier Selection** on an **Open** Transport Order when you want Shipper TMS to compare carriers for the current route.

The feature helps planners choose a carrier based on configured rates instead of manual estimates.

![Carrier Selection results](resources/carrierselection/screenshot-carrier-selection-results.png)

## Before you start

Make sure these items are in place:

1. **Carrier Selection Enabled** is turned on in [TMS Setup](setup.md).
2. [Carrier Rates](carrier-rates.md) exist for the carriers you want to compare.
3. **Carrier Rate Types Mapping** is configured in TMS Setup.
4. The Transport Order is **Open**.
5. Route stops are already defined.
6. If you want automatic charges, **Auto Create Charge Line** is enabled.

## Run Carrier Selection

1. Open the [Transport Order](transportorder.md).
2. Make sure the order status is **Open**.
3. Review route stops, addresses, and distance data.
4. Choose **Carrier Selection**.
5. Review the returned carrier rows.
6. Open or review the cost breakdown if needed.
7. Select the carrier you want to use.
8. Confirm that **Carrier No.** and **Carrier Name** are updated on the order.
9. If automatic charge creation is enabled, review [Transport Charges](transport-charges.md).

## What the comparison can include

The calculation can include:

- route-based rate amount,
- flat fee amount,
- fee per load,
- fee per unload,
- empty-return amount,
- carrier start or end map locations when configured on the carrier.

When you apply the result, the selected carrier is written back to the Transport Order.

If **Auto Create Charge Line** is enabled, Shipper TMS can also create charge lines on the order.

## If no good result appears

Check these items:

- the Transport Order is **Open**,
- carrier selection is enabled,
- the carrier is not blocked,
- the route has the stops you expect,
- map locations and distance data are usable,
- carrier start and end map locations are correct,
- the carrier has rates for the relevant geography,
- rate-type mapping is complete.

## Related

- [Carrier Rates](carrier-rates.md)
- [Carriers](carrier.md)
- [Transport Order](transportorder.md)
- [Transport Charges](transport-charges.md)
- [TMS Setup](setup.md)
