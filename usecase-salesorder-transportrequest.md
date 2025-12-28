# Use Case: Create Transport Request from Sales Order (Shipper)

## Problem
Need to hand a sales order off to transportation so dispatch can plan pickup, vehicle, and delivery. Without this step the order stays in sales and the transport team cannot schedule or allocate resources.

## Steps
1. Open `Sales Orders` from the Business Manager role center.
2. Click `New` to create a sales order that will be passed to TMS.
3. In `Sell-to Customer Name`, use lookup to select the correct customer (binds ship-to details).
4. On the lines, choose an item in `No.` (what needs to be shipped).
5. Set `Location Code` to the warehouse that will release goods (pickup point).
6. Enter `Quantity` (how many units will be transported).
7. Run `Create Transport Request` on the lines to send the order to TMS.
8. Confirm both prompts (`Yes`, `Yes`) to finalize creation and related updates.
9. The `Transport Request` page opens for transportation managers to continue planning (vehicle, time slots, routing).

## Outcome
A Transport Request is created and linked to the sales order. The transport team can now plan capacity, schedule loading/unloading, and include this request in a Transport Order.
