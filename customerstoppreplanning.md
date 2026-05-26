---
title: "Customer Stop Pre-Planner"
description: "Plan customer stops before creating or updating loads, sequence deliveries, review windows and warnings, and assign stops through Truck Load Management."
---

# Customer Stop Pre-Planner

Use **Customer Stop Pre-Planner** when a dispatcher wants to plan the visit order by customer stop instead of by individual transport condition lines.

The worksheet opens from an existing **Transport Order**, from **Transport Request Load Planning**, from a selected **Truck Load Management** slot, or directly from search / the Dispatcher Role Center for Transport Request pre-planning. It builds a temporary planning view and does not create a new business document.

The supported opening scenarios are:

- **Direct pre-planning** from search or the Dispatcher Role Center.
- **Existing trip planning** from a Transport Order.
- **Load Management planning** from Transport Request Load Planning.
- **Truck slot planning** from Truck Load Management.

## What it shows

Each row represents one customer stop. Several Transport Requests or Transport Lines can be grouped into one stop when they belong to the same consignee and unload point.

Transport conditions are shown as columns:

- weight by transport condition 1 to 4,
- volume by transport condition 1 to 4,
- other weight or volume when the condition is not configured in TMS Setup,
- total weight, volume, footage, and logistic units.

The worksheet also shows route context, delivery schedule, unload map location, delivery window, assigned vehicle context, warnings, and source document information.

The right side includes:

- **Current Trip Summary** for the current trip context,
- **Sources** with the Transport Requests or Transport Lines behind the selected stop,
- **Warnings** with stop-level issues such as missing delivery windows or missing map coordinates.

## How customer stops are grouped

Customer Stop Pre-Planner does not group all deliveries for the same customer into one monthly line. It groups data into stops inside the current planning context.

In **Transport Requests** mode, customer stops are grouped by:

- the planning date according to **Date Basis**,
- **Route No.**,
- **Delivery Schedule**,
- **Consignee Type**,
- **Consignee No.**,
- **Unload Address Code**,
- **Consignee Map Location No.**

This means the same customer can appear on several rows when the requests have different unload dates, route numbers, delivery schedules, unload addresses, or unload map locations. For example, if **Date Basis** is **Unload Date**, the same customer and address on March 11, March 12, and March 24 are shown as separate customer stops.

In **Transport Order** mode, customer stops are grouped by:

- **Transport Order No.**,
- consignee entity type and number,
- consignee sub-number / unload address context,
- unload waypoint / map location.

Carrier start and end route points are not shown as customer stops.

If a **Transport Condition** filter is set, the worksheet keeps only stops that contain at least one matching source line or request. Counts and totals then reflect only the matching underlying sources.

## Common workflow

Use the worksheet as a temporary planning surface:

1. Open Customer Stop Pre-Planner from one of the supported entry points.
2. Review the grouped customer stops.
3. Adjust filters such as Date Basis, planning period, Route No., or Show Mode when available.
4. Change **Sequence** manually or with one of the sequencing actions.
5. Select stop rows with the standard Business Central row selection when an assignment, move, or map-preview action should operate on several rows. If no row selection is active, selected-stop actions use the current row.
6. Use **Show Selected Route** to preview the selected customer stops on the map in the current Sequence order.
7. Use **Reschedule Selected Requests** when the load or unload date/time must be changed for all Transport Requests behind the selected stops.
8. Apply the sequence, build a Transport Order, assign stops to a truck slot, or move stops to another truck.

The page can be refreshed at any time with **Refresh**. Refresh rebuilds the temporary worksheet from current Transport Requests or Transport Order Lines.

## Sequence planning

Change the **Sequence** field to sketch the customer stop order. Manual edits do not automatically reorder the page.

Use:

- **Move Up** and **Move Down** for quick changes,
- **Renumber Sequence** to create clean 10, 20, 30 numbering,
- **Auto-sequence by Map Coordinates** for a nearest-neighbour draft based on unload map-location GPS coordinates, not provider road distance,
- **Show Selected Route** to open the selected customer stops on the map in the current Sequence order,
- **Apply Sequence** to write the route sequence back to the Transport Order.

Apply Sequence is allowed only while the Transport Order is **Open**. Shipper TMS applies the stop order through **Route Sequence** and then uses the existing route sequence optimization logic to rebuild Transport Lines.

This does not calculate a new road-optimized route and does not override the dispatcher order. The existing route sequence logic sorts Transport Lines by the Route Sequence that the dispatcher selected, then normalizes related load lines and carrier route points.

Map distance sequencing uses existing **TMAS Map Location** latitude and longitude values. If a vehicle has a default map location, that location is used as the route start; otherwise, the first stop with coordinates is used as the start. Stops without GPS coordinates are placed after mapped stops and marked with a warning.

Show Selected Route uses the selected stop rows and their current Sequence. It does not optimize or renumber the stops; it only shows the route on the map in the dispatcher-selected order. The preview starts from the first loading or start map location that can be found for the selection, then goes to the first selected unload stop and continues through the remaining selected unload stops. If only one unload stop is selected and no separate start point is available, the action opens that customer stop on the map.

## Delivery windows and warnings

Delivery window status is calculated from the unload time-slot profile and planned unload date/time. The worksheet supports day-specific profile lines, falls back to **Any Day** profile lines, and marks the stop as:

- **Inside** when the planned unload time is within a matching window,
- **Outside** when a window exists but the planned unload time is outside it,
- **Multiple** when several matching windows or stop-level profiles make the window ambiguous,
- **Missing** when no unload window is available.

The right side includes a **Warnings** FactBox that collects stop-level warnings, including outside delivery windows, mixed assignment context, multiple route sequences, and missing GPS coordinates for map-distance sequencing.

## Scenario 1: direct pre-planning

Open **Customer Stop Pre-Planner** directly from search or from the Dispatcher Role Center.

Use this scenario when the dispatcher starts from released Transport Requests and wants to sketch the customer-stop sequence before choosing a truck.

When opened directly, the worksheet starts in **Transport Requests** mode with:

- **Date Basis** = Unload Date,
- the current planning period from Load Management settings, or Work Date when no period is configured,
- **Show Mode** = Unassigned.

Typical steps:

1. Adjust **Date Basis** if needed. Use **Unload Date** for delivery-route planning, **Load Date** for loading-period planning, or **Planning Base Date** when that is the operational planning date.
2. Use **Previous Period**, **Set Planning Period**, or **Next Period** to choose the planning period.
3. Adjust **Route No.** if needed.
4. Keep **Show Mode** = Unassigned when the goal is to create or assign a new trip.
5. Choose **Refresh**.
6. Review one row per customer stop. Each row can include several underlying Transport Requests for different transport conditions.
7. Enter or adjust **Sequence**.
8. Optionally choose **Auto-sequence by Map Coordinates** to create a draft sequence from unload map-location GPS coordinates, then adjust manually.
9. Select the stop rows and choose **Show Selected Route** if you want to review the planned driving order on the map before assigning a truck.
10. Select the customer stop rows that should become part of the same truck assignment.
11. Choose **Create Draft Transport Order** if the trip should be created now but the truck is not known yet. If any selected stop has no sequence, the worksheet numbers the selected stops automatically as 10, 20, 30, and so on before creating the order.
12. Choose **Assign Stops to Truck Slot** if the truck slot is already known.
13. Select the target truck slot.
14. Confirm the Truck Load Management assignment.

If truck load slots do not exist for the selected period yet, the first **Assign Stops to Truck Slot** action prepares the slots and stops. Choose the action again to select the target slot.

The **Select Truck Slot** page for this action only shows slots that can still accept the selected Transport Requests or need planner review. Slots that are fully blocked by the existing Truck Load Management preview, for example because the request load datetime does not fit the truck slot time window, are hidden from this assignment selector. Use **Reschedule Selected Requests**, change the planning period, or review Truck Load Management if no target slot is offered.

Result:

- The selected Transport Requests are assigned through Truck Load Management.
- The Transport Order is created or updated by the existing truck-slot logic.
- Capacity, compartment, driver, status, and conflict checks are preserved.
- The stop sequence is written through Route Sequence.

When **Create Draft Transport Order** is used instead, the worksheet creates an Open Transport Order without a truck slot, vehicle, or driver. The selected stop sequence is saved to the Transport Requests and then applied to the new Transport Order through Route Sequence. Assign the truck later from the normal Transport Order / Truck Load Management flow.

Use **Apply Sequence to Transport Requests** when the dispatcher only wants to save the stop order on released Transport Requests without creating a Transport Order yet. This action is available for Unassigned mode.

Use **Reschedule Selected Requests** when selected customer stops need a new loading or delivery time before they are assigned to a truck. The action opens **Transport Request Reschedule** with all underlying Transport Requests from the selected stop rows. The wizard updates Open and Released requests, lets the dispatcher choose time values from the selected requests' time-slot profiles, shows time-slot warnings, and skips requests that are already Assigned.

## Scenario 2: existing Transport Order

From a Transport Order, choose **Customer Stop Planning**.

Use this scenario when the trip already exists and the dispatcher wants to review or adjust the customer-stop order.

The worksheet opens in **Transport Order** mode and groups customer unload Transport Lines into customer stops. Carrier start/end points are not shown as customer stops.

Typical steps:

1. Open an existing Transport Order.
2. Choose **Customer Stop Planning**.
3. Review the customer stops, delivery windows, transport condition totals, assigned vehicle context, source documents, and Current Trip Summary.
4. Change **Sequence** manually or with **Move Up**, **Move Down**, **Renumber Sequence**, or **Auto-sequence by Map Coordinates**.
5. Select at least two stops and choose **Show Selected Route** when the dispatcher wants to preview the current stop order on the map.
6. Choose **Apply Sequence**.

Result:

- Route Sequence is updated on the linked Transport Requests and Transport Lines.
- Existing route sequence logic rebuilds the technical Transport Line sequence.
- Related load lines and carrier route points remain aligned with the trip structure.

Rules:

- The Transport Order must be **Open**.
- Vehicle fields are read-only. Do not change the truck by editing a customer stop row.
- If the same Transport Request appears in multiple unload stops, Customer Stop Pre-Planner blocks Apply Sequence because this MVP cannot apply a different Route Sequence per waypoint of the same Transport Request.

Available follow-up actions:

- **Open Transport Order** returns to the trip.
- **Open Transport Requests**, **Open Transport Lines**, and **Open Source Documents** drill into the underlying records.
- **Move Selected Stops to Another Truck** moves selected customer stops through Truck Load Management.
- **Change Truck for Whole Transport Order** moves all stops of the current trip to another truck slot.

## Scenario 3: from Load Management

From **Transport Request Load Planning**, choose **Customer Stop View**.

Use this scenario when a dispatcher is already working in Load Management and wants a stop-level view of the same planning work.

The action chooses the most specific context available:

- If a Transport Order or an assigned request is selected, Customer Stop Pre-Planner opens the linked Transport Order.
- If no Transport Order context is selected, it opens unassigned Transport Requests for the current Load Date planning period.

Typical steps when a Transport Order is selected:

1. Select the Transport Order or an assigned request in Load Management.
2. Choose **Customer Stop View**.
3. Review the trip at customer-stop level.
4. Adjust and apply sequence as in Scenario 2.

Typical steps when no Transport Order is selected:

1. Open Load Management for the required planning period.
2. Choose **Customer Stop View** without selecting a specific Transport Order context.
3. Review unassigned Transport Requests grouped by customer stop.
4. Adjust sequence and select stop rows.
5. Choose **Assign Stops to Truck Slot** to assign selected stops to a truck slot.

Result:

- Dispatchers can move between request-first planning and customer-stop planning without losing the normal Truck Load Management guardrails.
- The same Date Basis, Show Mode, sequence, assignment, and source drill-down behavior is available as in direct pre-planning.

## Scenario 4: from Truck Load Management

From **Truck Load Management**, choose **Customer Stop Pre-Plan** on a truck slot.

Use this scenario when the dispatcher starts from a specific truck and time slot.

If the slot already has a linked Transport Order, Customer Stop Pre-Planner opens that Transport Order view.

If the slot is still empty, the worksheet shows released, unassigned Transport Requests grouped by customer stop for the same planning period that is currently open in Truck Load Management. The default date basis is **Load Date**, because the worksheet was opened from a truck loading slot. The user can switch the Date Basis filter to **Unload Date** when sketching a delivery-route view for a different delivery day.

Typical steps for an empty truck slot:

1. Open Truck Load Management.
2. Select the truck slot.
3. Choose **Customer Stop Pre-Plan**.
4. Review released, unassigned Transport Requests grouped by customer stop.
5. Adjust Date Basis, Route No., and sequence if needed. The planning period is inherited from Truck Load Management; choose another period there when another truck planning period is required.
6. Select the stops for this truck slot.
7. Choose **Assign Selected Stops to Truck Slot**.
8. Confirm the assignment.

Result:

- Truck Load Management evaluates every underlying Transport Request.
- If any request in a selected customer stop is blocked, the whole stop-level selection is blocked.
- Truck Load Management creates or updates the Transport Order for the slot.
- Customer Stop Pre-Planner refreshes to the Transport Order view when a Transport Order is available.

Typical steps for a slot that already has a Transport Order:

1. Open Truck Load Management.
2. Select the occupied truck slot.
3. Choose **Customer Stop Pre-Plan**.
4. Review and adjust the customer-stop sequence of the existing trip.
5. Choose **Apply Sequence**.

Result:

- The existing Transport Order remains the source of truth.
- Customer Stop Pre-Planner only changes stop sequence through Route Sequence.

## Filters and modes

Use the header filters to control the worksheet:

- **Date Basis**: Unload Date, Load Date, or Planning Base Date.
- **Planning Date From / Planning Date To**: the current planning period.
- **Route No.**: optional route filter.
- **Transport Condition**: optional condition filter. The worksheet keeps a customer stop visible when at least one underlying Transport Request or Transport Line has the selected condition, for example Frozen. When this filter is active, counts, totals, the Sources FactBox, and selected-stop actions use only the matching underlying sources. Clear the filter to work with the complete customer stop across all transport conditions.
- **Show Mode**: Unassigned, Assigned, or All.

Use **Previous Period**, **Set Planning Period**, and **Next Period** to change the planning period in Transport Requests mode. The current period is shown in the page title, matching Load Management, Truck Load Management, and the Visual Scheduler. When Customer Stop Pre-Planner is opened from a specific truck slot, the period is inherited from Truck Load Management; change the period in Truck Load Management when another truck planning period is required.

When the worksheet opens from a Transport Order that has a single transport condition on the header, the **Transport Condition** filter is filled from that Transport Order. When it opens from an empty Truck Load Slot, the filter is filled from the slot vehicle type only when the vehicle type or all configured compartments point to one clear transport condition.

Show Mode behavior:

- **Unassigned** shows released requests that are not assigned to a Transport Order.
- **Assigned** shows requests that are already assigned or in Transport status.
- **All** shows both released and assigned planning candidates.

Use **Assign Stops to Truck Slot** only from Unassigned planning. Assigned requests should be handled through the linked Transport Order or by using move actions.

Use **Create Draft Transport Order** when the dispatcher wants to create the Open Transport Order first and choose the truck later. This action is also only available from Unassigned planning. Missing sequence numbers on the selected stops are assigned automatically before the draft order is created.

## Move and reassignment

Use **Move Selected Stops to Another Truck** when selected stops are already assigned to one Open Transport Order and must move to another truck slot.

The worksheet moves customer stops as a whole. If a stop contains several Transport Requests for dry, cooled, or frozen conditions, all of those requests are evaluated and moved together. If one underlying request is blocked for the target slot, the whole selected stop-level move is blocked.

Use **Change Truck for Whole Transport Order** when the complete trip should move to another truck slot. This action builds the move selection from all customer stops in the current Transport Order, then uses the same Truck Load Management move flow.

Both actions use the existing Truck Load Management target-slot selection, capacity checks, compartment checks, status checks, and driver conflict checks.

If the target Transport Order already contains the same Route Sequence as a selected customer stop, Customer Stop Pre-Planner blocks the operation and asks the user to renumber the selected stops or the target trip first.

## Vehicle assignment

Assigned vehicle, vehicle type, driver, truck load planning date, and time slot are shown as read-only context.

Do not change the vehicle from a customer stop row. Truck and driver assignment remains controlled by Transport Order, Transport Request Load Planning, and Truck Load Management.

## What the user can do

Customer Stop Pre-Planner supports:

- grouping Transport Requests or Transport Lines into customer stops,
- reviewing condition-level weights and volumes as columns,
- reviewing delivery windows and warnings,
- reviewing Current Trip Summary,
- manually changing stop sequence,
- drafting sequence by map coordinates,
- previewing selected stops on the map in the current Sequence order,
- applying stop sequence to an Open Transport Order,
- saving sequence on released unassigned Transport Requests,
- rescheduling load or unload date/time for Transport Requests behind selected customer stops,
- building a Transport Order from selected customer stops,
- assigning selected stops to a truck slot,
- moving selected stops to another truck slot,
- changing the truck for a whole Transport Order,
- drilling down to Transport Requests, Transport Lines, source documents, consignee, map location, Load Management, and Truck Load Management.

## What it does not do

Customer Stop Pre-Planner does not:

- replace Transport Order, Load Management, or Truck Load Management,
- create a separate business document,
- edit Vehicle No. directly on a customer stop row,
- bypass capacity, compartment, driver, status, or truck-slot checks,
- split one customer stop by moving only one transport condition while leaving the other conditions on the old truck,
- calculate provider road-distance sequencing,
- show pallet or rolcontainer totals until a reliable logistic-unit-type mapping is available.

## Current scope

This release supports Customer Stop Pre-Planner from an existing Transport Order, from Transport Request Load Planning, from Truck Load Management truck slots, as direct Transport Request pre-planning, and for stop-level move / reassignment between truck slots. Current Trip Summary is selection-aware in multi-trip/request views, so the FactBox summarizes the current trip context instead of always showing the whole worksheet.

Pallet or rolcontainer totals are outside this scope until a reliable logistic-unit-type mapping is confirmed.
