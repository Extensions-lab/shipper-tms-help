---
title: "Zones"
description: "Use Zones to group locations geographically and connect internal zone logic with telematics geofences in Shipper TMS."
---

# Zones

Use **Zones** when your company wants to plan and classify transportation by geographic area instead of only by address.

Typical zone examples:

- depot areas,
- delivery regions,
- warehouse yards,
- terminal zones,
- telematics geofences.

## How to work in this page

Use the Zone card when the business needs planning areas or geofence-style grouping.

1. Fill **Code**, **Description**, and **Type Code** in **General**.
2. Keep **Active** turned on only for zones that should be used.
3. Choose the main geometry type in **Primary Geometry**.
4. For a circle, fill center latitude, center longitude, and radius.
5. For a polygon, maintain points in **Zone Points**.
6. Use **Additional Geometries** when the zone has multiple areas or holes.
7. Set default carrier, vehicle, or driver only when this zone usually uses those resources.
8. Use **Zone Carriers** when more than one carrier serves the zone.
9. Choose **Show on Map** to visually review the geometry.

## Two zone layers you should know about

| Layer | Purpose |
|---|---|
| **Zone** | Your internal Shipper TMS zone used for planning and master data |
| **Telematics Zone** | Provider snapshot imported from Geotab, Samsara, or Webfleet |

This separation lets you keep your own business structure while still connecting to external geofences.

## Use zones for planning and rating

Use standard zones when the business needs simple geographic classification.

Common uses include:

- assigning a default carrier, vehicle, or driver for an area,
- filtering or grouping transport demand,
- supporting route and delivery-region planning,
- using zone-carrier relationships for service coverage,
- reporting demand by region.

For this use, a zone can be useful even before detailed geometry is maintained.

## Use zone geometry for maps, routing, and geofence scenarios

Use zone geometry when the system or integration needs a physical area, not just a code.

| Geometry option | Use it when |
|---|---|
| Circle | A depot, yard, or stop can be represented by a center point and radius |
| Polygon | A delivery area, terminal, or city region needs a precise boundary |
| Additional geometries | One business zone has multiple areas or exclusion holes |

Telematics integrations can synchronize provider geofences into telematics zone records. Map or review those records before relying on them for dispatch or execution logic.

## Create an internal zone

1. Search for **Zones**.
2. Choose **New**.
3. Fill in **Code**, **Description**, and **Type Code**.
4. Set **Active**.
5. Choose the geometry style:
   - circle,
   - polygon.
6. Enter the geometry data.
7. If needed, set default carrier, vehicle, or driver values for the zone.

## Advanced geometry

Use additional geometries when one zone needs:

- multiple separate areas,
- or a hole inside a larger area.

This is useful for complex yards, terminals, or city regions.

## Link a zone to a Map Location

1. Open the [Map Location](maplocation.md).
2. Make sure the location has coordinates.
3. Choose **Assign Zone** or fill the zone reference directly.

After that, the Map Location can be used with a geographic zone context during planning and integration.

## Zones and telematics

If you use [Telematics](telematics.md):

- provider zones can be synchronized into **Telematics Zones**,
- internal zones can be mapped to those external zones,
- published stops can use the mapped geofence reference.

## Sync policy

Use the zone **Sync Policy** to decide how external updates should behave:

- keep the zone fully manual,
- import once and maintain internally,
- mirror the external provider,
- or allow manual override.

## Related

- [Map Locations](maplocation.md)
- [Telematics](telematics.md)
- [Transport Order](transportorder.md)
