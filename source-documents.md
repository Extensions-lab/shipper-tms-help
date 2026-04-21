---
title: "Source Documents"
description: "Use sales, purchase, transfer, and posted Business Central documents as the source of transport demand in Shipper TMS."
---

# Source documents

A **source document** is the Business Central document that creates transport demand.

Shipper TMS can create or show Transport Requests and Transport Orders from sales, purchase, transfer, and selected posted documents.

![TMS actions on a source document](resources/source-documents/screenshot-source-document-actions.png)

## Supported source types

| Area | Supported source documents |
|---|---|
| **Sales** | Sales Order, Sales Invoice, Sales Credit Memo, Sales Return Order, Posted Sales Invoice, Posted Sales Shipment, Posted Sales Return, Posted Sales Credit Memo |
| **Purchase** | Purchase Order, Purchase Invoice, Purchase Credit Memo, Purchase Return Order, Posted Purchase Invoice, Posted Purchase Receipt, Posted Purchase Return, Posted Purchase Credit Memo |
| **Transfer** | Transfer Order, Posted Transfer Shipment, Posted Transfer Receipt |

The exact action set depends on the document type and status.

## What Shipper TMS adds

On supported document pages, Shipper TMS adds transport fields and actions such as:

- **Transportation Status**,
- **Create Transport Request**,
- **Split Order for Transportation**,
- **Transport Requests**,
- **Create Transport Order**,
- **Transport Orders**,
- TMS fields for route, route sequence, zone, map location, delivery schedule, and time slot where relevant.

## Create requests from a source document

Use this path when the remaining eligible lines can become Transport Requests without manual splitting.

1. Open the source document.
2. Make sure the document is **Released** when it is an unposted sales, purchase, or transfer document.
3. Choose **Create Transport Request**.
4. Confirm the result.
5. Open **Transport Requests** to review the created request.

## Split source lines across requests

Use this path when only part of the document should be planned now or when one document must become several transport requests.

1. Open the source document.
2. Choose **Split Order for Transportation**.
3. Review the source lines in the upper part of the worksheet.
4. Enter **Qty. to Add** for the quantities you want to plan.
5. Choose **New Transport Request** or **Add to Existing Transport Request**.
6. Release the requests when they are ready for planning.

For the full workflow, see [Transport Request Planning Worksheet](transport-request-planning.md).

## Transportation Status values

| Status | Meaning |
|---|---|
| *(blank)* | No transport activity exists yet |
| **Partial Transport Request** | Some quantity is assigned to Transport Requests |
| **Transport Request** | All relevant quantity is assigned to Transport Requests |
| **Partial Transport** | Some quantity is already assigned to a Transport Order |
| **Transport** | All relevant quantity is assigned to Transport Orders |
| **Delivered** | Transport execution is complete |

## Good to know

- Manual request creation from unposted source documents requires the source document to be **Released**.
- **Create Transport Request** is for remaining eligible quantities.
- **Split Order for Transportation** is for partial quantities and controlled distribution.
- Posted documents are useful when transport planning starts after posting.
- Customer, vendor, location, ship-to, and order-address map data improve automatic route creation.

## Related

- [Transport Request](transportrequest.md)
- [Transport Request Planning Worksheet](transport-request-planning.md)
- [Transport Order](transportorder.md)
- [Map Locations](maplocation.md)
