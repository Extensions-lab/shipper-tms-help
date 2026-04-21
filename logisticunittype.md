---
title: "Logistic Unit Types"
description: "Use Logistic Unit Types to define standard container and equipment capacity profiles that support Shipper TMS planning."
---

# Logistic Unit Types

**Logistic Unit Types** belong to the related Logistic Units extension, but they are important for Shipper TMS because they provide the capacity profile used by vehicles and planning logic.

Use them to define standard equipment such as:

- pallets,
- boxes,
- containers,
- trailers,
- transport unit profiles.

## How to work with this setup

Use Logistic Unit Types before you depend on capacity planning.

1. Define the unit types your operation actually uses.
2. Fill weight limits when weight control is enabled.
3. Fill volume and dimensions when volume control is enabled.
4. Fill footage when floor-space planning matters.
5. Turn on strict controls only when the system should prevent exceeding the limit.
6. Assign a transportation condition value when the unit type or compartment is dedicated to a condition such as Frozen or Ambient.
7. Assign the unit type to vehicles or vehicle configurations that use that capacity profile.
8. Test a Transport Order or Truck Load Management slot to confirm load percentages look right.

## When this matters in Shipper TMS

This setup matters when you want consistent:

- weight limits,
- volume limits,
- footage,
- logistic unit calculations,
- compartment or condition behavior.

## What to maintain

Review these areas on the Logistic Unit Type:

| Area | Why it matters |
|---|---|
| **Weight** | Controls payload and total weight logic |
| **Dimensions** | Supports volume and capacity calculations |
| **Control** | Defines whether strict limits should be enforced |
| **Transportation condition field** | Helps match equipment to compatible cargo when used |

## Important note

This page is not part of the Shipper TMS app alone. If your users need full instructions for the Logistic Units extension, maintain those instructions separately and link to them from your customer help site.

## Related

- [Vehicles](vehicle.md)
- [Transportation Conditions](transportationconditions.md)
- [Transport Order](transportorder.md)
