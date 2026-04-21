---
title: "Warehouse Documents"
description: "Create and review warehouse shipments and warehouse receipts from a Released Transport Order."
---

# Warehouse Documents

Use **Create Warehouse Documents** when warehouse work should be created from a Transport Order.

Shipper TMS can create:

- warehouse shipments for source lines that require shipment handling,
- warehouse receipts for source lines that require receipt handling.

![Warehouse document actions on a Transport Order](resources/warehouse-documents/screenshot-warehouse-document-actions.png)

## Before you start

1. The Transport Order must be **Released**.
2. The order must contain Transport Requests.
3. Source documents must be eligible for warehouse shipment or receipt creation.
4. Business Central warehouse setup must require warehouse documents for the relevant location.

## Create warehouse documents

1. Open the [Transport Order](transportorder.md).
2. Confirm the order status is **Released**.
3. Choose **Create Warehouse Documents**.
4. Confirm the action.
5. Open **Show Warehouse Shipments** or **Show Warehouse Receipts**.
6. Process the warehouse documents according to your warehouse workflow.

## What happens if documents already exist

If warehouse documents already exist, Shipper TMS opens the existing documents instead of creating duplicates.

The same applies when posted warehouse shipment or receipt records already exist for the Transport Order.

## Related

- [Transport Order](transportorder.md)
- [Source Documents](source-documents.md)
- [Reports and Documents](reports.md)
