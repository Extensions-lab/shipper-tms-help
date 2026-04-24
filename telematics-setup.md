---
title: "Telematics Setup"
description: "Create and maintain telematics setup records, provider credentials, and synchronization options."
---

# Telematics Setup

Use **Telematics Setup** to define the connection to a provider account.

## Before you start

- Decide which provider to use: **Geotab**, **Samsara**, or **Webfleet**.
- Get the provider base URL, account or tenant identifier, user name, and password or token.
- Create the Shipper TMS carrier, vehicle, and driver records that will be mapped.
- Assign telematics permission sets to the admin or integration account.

## Create a setup record

1. Search for **Telematics Setup**.
2. Choose **New**.
3. Fill **Code** and **Description**.
4. Select **Provider**.
5. Turn on **Enabled** when the record is ready for use.
6. Fill provider connection fields such as **Base URL**, **Account ID**, **Database Name**, and **User Name**.
7. Store the password or token using the provider secret action where available.
8. Turn on the sync streams your company uses.
9. Test the provider connection.

![Telematics provider setup](resources/telematics/screenshot-telematics-provider-setup.png)

## Provider setup notes

| Provider | Pay special attention to | Good first test |
|---|---|---|
| **Geotab** | Database name, user name, password/secret, and vehicle/driver external IDs | Sync vehicles or current positions |
| **Samsara** | API token, route webhook registration, and external IDs used for vehicles and drivers | Register the route webhook, then sync vehicles |
| **Webfleet** | Account credentials, route queue setup, and queue cleanup process | Ensure the route queue, then publish a test dispatch |

Use one enabled setup record per provider account that Shipper TMS should talk to. If your company uses several provider tenants or regions, create separate setup records with clear codes and descriptions.

## Important fields

| Field | What it controls |
|---|---|
| **Provider** | Geotab, Samsara, or Webfleet implementation |
| **Enabled** | Whether the setup can be used for sync or dispatch |
| **Authentication Type** | Authentication model expected by the provider |
| **Base URL** | Provider API base address |
| **Account ID** | Provider account, tenant, or company identifier |
| **Database Name** | Provider database name when required, especially for Geotab |
| **User Name** | Provider user name or service account |
| **Sync Vehicles** | Vehicle master data synchronization |
| **Sync Drivers** | Driver master data synchronization |
| **Sync Zones** | Geofence or provider-zone synchronization |
| **Sync Driver Vehicle Assignments** | Driver-to-vehicle assignment synchronization |
| **Sync Current Positions** | Latest known vehicle positions |
| **Sync Position History** | Historical GPS positions |
| **Sync Trips** | Trip summaries |
| **Sync Routes / Dispatches** | Provider routes and dispatches |
| **Sync Trailer / Assets** | Trailer and asset records |
| **Sync HOS / ELD** | Hours-of-service and ELD availability data |
| **Background Polling Enabled** | Whether the setup can poll provider data in the background |
| **Polling Interval (sec.)** | Normal polling interval |
| **Recovery Interval (sec.)** | Retry interval after recoverable failures |

## Security note

Do not store provider passwords, API tokens, or webhook secrets in notes, screenshots, or plain-text documentation. Use the secret action on the setup page and follow your company's credential rotation policy.

## Related

- [Telematics provider mapping](telematics-provider-mapping.md)
- [Telematics sync and logs](telematics-sync-and-logs.md)
- [Assign Permission Sets](assignpermissionsets.md)
- [API](api.md)
