---
title: "Transport Request"
description: "Use Transport Requests to capture what must be moved, from where, to where, and when in Shipper TMS."
---

# Transport Request

A **Transport Request** is the planning document in Shipper TMS.

It answers four questions:

- what must be moved,
- from where,
- to where,
- and when.

Use a Transport Request before you build the trip in a [Transport Order](transportorder.md).

![Transport Request example showing load point, unload point, and route actions](resources/transportrequest/tr5.png)

## What a Transport Request contains

A Transport Request can contain:

- source document lines,
- shipper and consignee information,
- load and unload dates,
- route and route sequence,
- transportation condition,
- calculated totals such as weight, volume, footage, and estimated logistic units.

## How requests are created

| Method | Use it when |
|---|---|
| **Automatic creation from released documents** | TMS Setup is configured to create requests during document release |
| **Create Transport Request** on a source document | The remaining eligible quantities should become requests immediately |
| **Split Order for Transportation** | You need partial quantities or several requests from one document |
| **Get Source Documents** on a request | You want to add more released source lines to an Open request |
| **Document lists** | You want to create requests for several documents in bulk |

For supported document types, see [Source Documents](source-documents.md).

## Statuses

| Status | Meaning |
|---|---|
| **Open** | The request can still be prepared and adjusted |
| **Released** | The request is ready for planning |
| **Transport** | The request is assigned to a Transport Order |

## Important rules

- Only **Released** requests can be assigned to a Transport Order.
- A request in **Transport** status is no longer available in the free planning pool.
- If the request is removed from the Transport Order, it can return to **Released**.
- For unposted source documents, manual creation from the document card requires the source document to be **Released**.

## How to work in this window

1. Review the **General** section and confirm the request status.
2. Review **Shipper** and **Consignee**.
3. Fill or adjust load and unload date/time values while the request is still **Open**.
4. Review **Lines**.
5. If you need to add more source lines, choose **Get Source Documents** while the request is **Open**.
6. If map locations are filled, choose **Show Route**.
7. Choose **Transport Time & Distance** to calculate distance and duration.
8. Choose **Estimate** when logistic unit estimation should be rebuilt.
9. Choose **Release** when the request is ready for planning.
10. Choose **Assign to Transport Order** when you want to place this request into an existing Transport Order.
11. If the request is already assigned, choose **Show Transport** to open the related order.

Use the list page when you want to release, reopen, or assign multiple requests at the same time.

## Useful actions

| Action | Use it for |
|---|---|
| **Get Source Documents** | Add more released lines while the request is still Open |
| **Show Route** | Display the route on the map |
| **Transport Time & Distance** | Calculate distance and duration |
| **Release** | Move the request to Released |
| **Reopen** | Move the request back to Open |
| **Assign to Transport Order** | Add the request to an existing order |
| **Show Transport** | Open the linked Transport Order |
| **Estimate** | Rebuild estimated logistic units |

## Typical workflow

1. Create the request from a source document.
2. Review addresses, route, dates, and totals.
3. Release the request.
4. Assign it to a Transport Order directly or through a planning tool.

## Related

- [Source Documents](source-documents.md)
- [Transport Request Planning Worksheet](transport-request-planning.md)
- [Transport Order](transportorder.md)
- [Load Management](loadmanagement.md)
- [Truck Load Management](truckloadmanagement.md)
