---
title: "Map Providers"
description: "Choose and configure Google Maps or Azure Maps for geocoding, routing, and distance calculations in Shipper TMS."
---

# Map providers

Shipper TMS uses a map provider for:

- geocoding addresses,
- showing routes on a map,
- calculating distance and duration,
- route optimization,
- route-distance caching.

![Map provider settings in Shipper TMS Setup](screenshot-map-providers-setup.png)

## How to work with map provider setup

Use this setup before users calculate distances or show routes.

1. Decide which provider your company will use.
2. Configure the provider account outside Business Central.
3. Open **Shipper TMS Setup**.
4. Select **Map Provider**.
5. Enter the required provider key.
6. Create or update Map Locations so important stops have coordinates.
7. Test **Geocode address** on a Map Location.
8. Test **Show Route** or **Get Transport Time & Distance** from a Transport Request or Transport Order.
9. If using Azure Maps for truck-aware routing, configure vehicle routing profiles before relying on truck restrictions.

## Which provider should you choose

| Provider | Best when |
|---|---|
| **Google Maps** | You need standard address geocoding and road routing |
| **Azure Maps** | You need truck-aware routing with vehicle restrictions |

## Configure the provider in TMS

1. Open **Shipper TMS Setup**.
2. Go to **Map Provider Settings**.
3. Select **Map Provider**.
4. Enter the required key:
   - **Google Api Key**
   - or **Azure Maps Subscription Key**
5. For Azure Maps, also select **Azure Maps Geo Scope** if your company needs a specific processing region.

## When to use Azure Maps vehicle routing profiles

If you use **Azure Maps** and want truck-aware routing:

1. Open **Vehicle Routing Profiles**.
2. Create a profile or use **Set Default Vehicle Routing Profiles**.
3. Assign the routing profile on the relevant vehicle unit type.
4. Use that vehicle type on the Transport Order.

This is how Azure Maps can consider vehicle size, weight, axle, and hazardous-load restrictions during route calculation.

## Troubleshooting

If routing or geocoding does not work:

1. Verify that **Map Provider** is selected in **Shipper TMS Setup**
2. Verify the key is entered correctly
3. Verify the map location has a usable address or coordinates
4. If you expect truck-aware routing, verify that:
   - the provider is **Azure Maps**
   - the vehicle type is filled on the Transport Order
   - the vehicle type has a routing profile

## Step-by-step setup guides

- For Google-specific setup, see [Google Maps integration](googlemapintegration.md)
- For Azure-specific setup, see [Azure Maps integration](azuremapsintegration.md)

## Related

- [Google Maps integration](googlemapintegration.md)
- [Azure Maps integration](azuremapsintegration.md)
- [Map Locations](maplocation.md)
- [Transport Request](transportrequest.md)
- [Transport Order](transportorder.md)
