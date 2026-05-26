---
title: "Time Slots and Delivery Schedules"
description: "Use Shipper TMS time slot profiles and delivery schedules to calculate planned load and unload dates, assign windows, and automate transport timing rules."
---

# Time slots and delivery schedules

Use this setup when your company wants Shipper TMS to calculate planned transportation timing automatically.

The setup has two parts:

- **Delivery Schedule** decides the date
- **Time Slot Profile** decides the time window on that date

![Transport Request timeline with load and unload time slots](resources/transportrequest/tr8.png)

## How to work with these pages

Use these pages together.

1. Create the **Time Slot Profile** first.
2. Add time-slot lines for the real receiving or loading windows.
3. Use **Day of Week** when a time window applies only on specific days.
4. Use an "any day" style slot only when the same time works every day.
5. Create the **Delivery Schedule** that calculates the date.
6. Assign the delivery schedule and time-slot profile to the customer, vendor, location, ship-to address, or order address.
7. Create a test Transport Request and confirm that load/unload date and time values are calculated as expected.

## Create a Time Slot Profile

1. Search for **Time Slot Profiles**.
2. Choose **New**.
3. Fill in **Code** and **Description**.
4. Open the profile lines.
5. Add one or more time slots with:
   - **No.**
   - **Description**
   - **Time Start**
   - **Time End**
   - **Day of Week**

## Create a Delivery Schedule

1. Search for **Delivery Schedules**.
2. Choose **New**.
3. Fill in:
   - **Base Date**
   - **Second Base Date**
   - **Base Date Mandatory**
   - **Lead Time**
   - **Calendar**

## Assign the setup to master data

Apply the schedule and time-slot profile on the relevant:

- customer,
- vendor,
- location,
- ship-to address,
- order address.

## How the system chooses the final time

When a Transport Request is created:

1. Shipper TMS calculates the target date from the delivery schedule.
2. It looks for a matching time slot on that day of week.
3. If no day-specific slot exists, it falls back to the best available default logic.

## Example

If a customer accepts deliveries only on Monday and Thursday:

- the delivery schedule can use a calendar that allows only those days,
- the time-slot profile can define separate Monday and Thursday windows,
- newly created Transport Requests will follow that pattern automatically.

## Related

- [TMS Setup](setup.md)
- [Transport Request](transportrequest.md)
- [Truck Load Management](truckloadmanagement.md)
