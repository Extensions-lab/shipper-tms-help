---
title: "Transport Request Planning Worksheet"
description: "Distribute source document lines across one or more Transport Requests."
---

# Transport Request Planning Worksheet

Use **Transport Request Planning Worksheet** when one source document must be split across one or more Transport Requests.

Use it when you need to:

- create requests for only part of a document,
- split one order into several deliveries,
- add remaining quantities to an existing Open request,
- move quantities between Open requests,
- release or reopen all related requests from one page.

![Transport Request Planning Worksheet](/resources/transport-request-planning/screenshot-transport-request-planning-worksheet.png)

## How the page is organized

| Area | Purpose |
|---|---|
| **Source Lines** | Shows source quantities, posted quantities, distributed quantities, remaining quantities, and **Qty. to Add** |
| **Planned Transport Requests** | Shows the Transport Requests and request lines already created for this source document |
| **Transport Request Summary** | Shows totals for the selected request |

## Create a new request from selected quantities

1. Open the source document.
2. Choose **Split Order for Transportation**.
3. In **Source Lines**, enter **Qty. to Add** on the lines you want to plan.
4. Choose **New Transport Request**.
5. Review the created request number or request count.
6. Release the request when it is ready for planning.

## Add quantities to an existing request

Use this when an Open Transport Request already exists for the same source document.

1. Enter **Qty. to Add** on the source lines.
2. Choose **Add to Existing Transport Request**.
3. Select the Open Transport Request.
4. Confirm the added lines in **Planned Transport Requests**.

## Move quantity to another request

1. In **Planned Transport Requests**, select a request line.
2. Choose **Move to Another TR**.
3. Select the target Open Transport Request.
4. Enter the quantity to move.
5. Refresh the worksheet and verify the balances.

## Useful actions

| Action | Use it for |
|---|---|
| **Fill Quantity** | Set **Qty. to Add** to the remaining quantity on all source lines |
| **Clear Quantity** | Set **Qty. to Add** to zero on all source lines |
| **New Transport Request** | Create request(s) from selected source lines |
| **Add to Existing Transport Request** | Add selected quantities to an Open request |
| **Refresh** | Recalculate source and distribution balances |
| **Release All** | Release all Open requests for this source document |
| **Reopen All** | Reopen Released requests that are not assigned to a Transport Order |

## Rules

- **Qty. to Add** cannot be negative.
- **Qty. to Add** cannot exceed **Remaining Qty.**.
- You can move quantities only to Open requests.
- Released requests must be reopened before you change their lines.
- Requests already assigned to a Transport Order cannot be reopened from this worksheet.

## Related

- [Source Documents](source-documents.md)
- [Transport Request](transportrequest.md)
- [Load Management](loadmanagement.md)
- [Truck Load Management](truckloadmanagement.md)
