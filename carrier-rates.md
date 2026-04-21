---
title: "Carrier Rates"
description: "Maintain carrier rate records used by Carrier Selection on Transport Orders."
---

# Carrier Rates

Use **Carrier Rates** to define how a carrier should be priced during [Carrier Selection](carrierselection.md).

A rate can include:

- route-based rate amount,
- flat fee,
- fee per load,
- fee per unload,
- empty-return rate,
- geographic filters such as region, country, county, city, or post code.

![Carrier Rates page](resources/carrier-rates/screenshot-carrier-rates.png)

## Before you start

Complete these setup items first:

1. Create the [Carrier](carrier.md).
2. Configure [Map Providers](mapproviders.md) if you want distance-based rates.
3. Enable carrier selection in [TMS Setup](setup.md).
4. Configure **Carrier Rate Types Mapping** in TMS Setup.

## Create a carrier rate

1. Open **Carriers**.
2. Open the carrier card.
3. Choose **Carrier Rates**.
4. Create a new line.
5. Fill the origin and destination filters that define where the rate applies.
6. Fill the pricing fields your company uses.
7. Repeat for each lane, geography, or fee rule.

## Main pricing fields

| Field | Use |
|---|---|
| **Rate** | Distance-based rate used for the main route |
| **Empty Return Rate** | Rate used for return distance or empty return logic |
| **Flat Fee** | Fixed amount added once for the matching rate |
| **Fee Per Load** | Charge added for loading activity |
| **Fee Per Unload** | Charge added for unload stops |
| **Charge Last Stop** | Controls whether the unload fee also applies to the final stop |

## Geographic matching

Use the origin and destination filters to make a rate more specific.

Start broad, then add specific rates only where they are needed:

1. country,
2. region or county,
3. city,
4. post code.

Avoid duplicate overlapping rates unless your carrier-pricing policy intentionally needs them.

## Verify the rate

1. Open a test [Transport Order](transportorder.md) with route stops.
2. Make sure the order is **Open**.
3. Choose **Carrier Selection**.
4. Confirm that the carrier appears.
5. Review the calculated amount and cost breakdown.

## Troubleshooting

| Problem | Check |
|---|---|
| Carrier does not appear | Carrier is blocked or not eligible |
| Amount is zero | No matching rate exists or only a fallback comparison row was created |
| Rate is too high or too low | Distance, empty-return setup, fees, and geographic filters |
| Auto charge line is missing | **Auto Create Charge Line** and **Carrier Rate Types Mapping** in TMS Setup |

## Related

- [Carriers](carrier.md)
- [Carrier Selection](carrierselection.md)
- [Transport Charges](transport-charges.md)
- [TMS Setup](setup.md)
