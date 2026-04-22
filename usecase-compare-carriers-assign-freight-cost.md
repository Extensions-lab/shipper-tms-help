---
title: "Use Case: Compare Carriers and Assign Freight Cost"
description: "Compare carrier rates, apply a carrier, and allocate freight cost on a Transport Order."
---

# Use case: Compare carriers and assign freight cost

## Goal

Select a carrier by rate and allocate the resulting freight cost so posting is not blocked.

## When to use it

Use this flow when carrier freight charges must be visible on the Transport Order and assigned to source document lines.

## Before you start

- Carrier Selection is enabled.
- Carrier Rates and Carrier Rate Types Mapping are configured.
- The Transport Order is **Open** and has route stops.
- Source documents are ready for item-charge assignment if charges must flow back to sales or purchase documents.

## Steps

1. Open the Transport Order.
2. Choose **Carrier Selection**.
3. Review the carrier rows and cost breakdown.
4. Apply the selected carrier.
5. Go to the **Charges** section.
6. Select the created charge line.
7. Choose **Show Assignment**.
8. Suggest allocation by distance, weight, volume, footage, logistic units, or equally.
9. Review and adjust amounts.
10. Choose **Apply** when source document item-charge assignment must be updated.

## Expected result

- The carrier is assigned to the order.
- Freight charge lines show assigned amounts.
- Required source document item-charge assignments are updated.

## What to do next

Release the order or continue planning route, warehouse, and execution details.

## Common errors

| Problem | What to check |
|---|---|
| Auto charge line is missing | Auto Create Charge Line, carrier vendor source, and rate type mapping |
| Assigned amount is not complete | Reopen Show Assignment and assign remaining amount |
| Posting is blocked | Source charge lines, item-charge assignment, and unposted sales or purchase documents |

## Related

- [Carrier Selection](carrierselection.md)
- [Transport Charges](transport-charges.md)
- [Transport Order](transportorder.md)
