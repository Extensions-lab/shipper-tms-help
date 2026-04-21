---
title: "Vehicle Routing Profiles"
description: "Use Vehicle Routing Profiles to define Azure Maps truck-routing constraints for logistic unit types."
---

# Vehicle Routing Profiles

Use **Vehicle Routing Profiles** when Azure Maps should calculate routes with truck restrictions.

A routing profile can describe:

- travel mode,
- commercial vehicle flag,
- vehicle dimensions,
- weight,
- axle weight,
- hazardous-load category,
- ADR tunnel restriction,
- road features to avoid,
- traffic usage,
- route instruction language.

![Vehicle Routing Profile card](resources/vehicle-routing-profiles/screenshot-vehicle-routing-profile-card.png)

## Before you start

1. Configure [Azure Maps Integration](azuremapsintegration.md).
2. Confirm that **Map Provider** is **Azure Maps** in [TMS Setup](setup.md).
3. Review your equipment types and restrictions.

## Create default profiles

1. Search for **Vehicle Routing Profiles**.
2. Choose **Set Default Vehicle Routing Profiles**.
3. Review the created profiles.
4. Adjust dimensions, weight, hazardous-load, and avoid settings to match your fleet.

## Assign a profile to a unit type

1. Open [Logistic Unit Types](logisticunittype.md).
2. Open the unit type that represents the vehicle or equipment profile.
3. Fill **Vehicle Routing Profile Code**.
4. Review dimensions and maximum weight.
5. Save the record.

## Use the profile on a route calculation

1. Use a vehicle or unit type that has a routing profile.
2. Add it to a Transport Order.
3. Run **Get Transport Time & Distance** or a route action.
4. Review the calculated route.

## Good to know

- Vehicle routing profiles are used with Azure Maps truck-aware routing.
- Google Maps setup does not use these truck-specific profile fields in the same way.
- Changing a profile can make stored route-distance values outdated.
- Recalculate route distance and duration after changing a routing profile.

## Related

- [Azure Maps Integration](azuremapsintegration.md)
- [Map Providers](mapproviders.md)
- [Logistic Unit Types](logisticunittype.md)
- [Distance Matrix](distance-matrix.md)
- [Transport Order](transportorder.md)
