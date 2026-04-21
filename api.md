---
title: "API"
description: "Use Shipper TMS API pages for integrations with carriers, vehicles, transport orders, execution entries, telematics, and attachments."
---

# API

Shipper TMS exposes Business Central API pages for integration scenarios.

Use the API when another system must create, read, or update transport data without using the Business Central user interface.

![API integration overview](resources/api/screenshot-api-overview.png)

## API identity

| Setting | Value |
|---|---|
| Publisher | `extensionslab` |
| API group | `stms` |
| Version | `v1.0` |

## Main API entity sets

| Entity set | Use |
|---|---|
| `carriers` | Carrier master data |
| `drivers` | Driver master data |
| `vehicles` | Vehicle master data |
| `maplocations` | Map locations and coordinates |
| `transportorders` | Transport Order headers |
| `transportorderlines` | Transport Order lines and route-related detail |
| `transportrequestlines` | Transport Request line data |
| `logisticunits` | Logistic unit headers |
| `logisticunitlines` | Logistic unit line data |
| `executionentries` | Delivery and execution facts |
| `executionentryattachments` | Execution-entry attachment metadata and file content actions |
| `telematicsSetups` | Telematics setup records |
| `telematicsAdmins` | Telematics administration actions |

## Attachment actions

The execution-entry attachment API supports service actions for:

- downloading attachment content,
- uploading base64 attachment content with description and MIME type.

Use these actions for proof-of-delivery photos, signed documents, or delivery evidence that must be attached to an execution entry.

## Telematics administration actions

Telematics admin API actions support provider-administration tasks such as:

- registering a Samsara route webhook,
- deleting a Samsara route webhook,
- ensuring a Webfleet route queue,
- deleting a Webfleet route queue,
- retrieving a route-ingress contract.

Telematics setup API actions can receive webhooks from provider integrations.

## Permissions

Assign integration accounts the minimum permission sets they need:

| Integration type | Permission set |
|---|---|
| General Shipper TMS API integration | **Shipper TMS - API** |
| Telematics webhook or data integration | **Shipper TMS - Tel. API** |
| Telematics administration integration | **Shipper TMS - Tel. Admin API** |

For user-facing setup, see [Assign Permission Sets](assignpermissionsets.md).

## Security guidance

- Use a dedicated service account.
- Assign only the required Shipper TMS API permission sets.
- Store credentials in an approved secret store.
- Do not reuse personal user accounts for integrations.
- Log integration errors outside the production UI where support teams can review them.

## Related

- [Assign Permission Sets](assignpermissionsets.md)
- [Telematics](telematics.md)
- [Execution Entries](execution-entries.md)
- [Transport Order](transportorder.md)
