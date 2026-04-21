---
title: "Assign Permission Sets"
description: "Assign the correct Shipper TMS permission sets to users, administrators, and integration accounts."
---

# Assign permission sets

After the app is installed and licenses are assigned, give users access to Shipper TMS by assigning the correct permission sets in Business Central.

![Add Shipper TMS permission sets on the user card](resources/assignpermissionset/screenshot-permissions-user-permission-sets.png)

## Which permission set to use

| Use this when | Permission set |
|---|---|
| Daily planning and execution | **Shipper TMS - User** |
| Setup and administration | **Shipper TMS - Administrator** |
| API integration | **Shipper TMS - API** |
| Telematics API access | **Shipper TMS - Tel. API** |
| Telematics admin API access | **Shipper TMS - Tel. Admin API** |

## Recommended assignment pattern

- Planners and dispatchers: **Shipper TMS - User**
- System administrators: **Shipper TMS - User** and **Shipper TMS - Administrator**
- Integration/service accounts: **Shipper TMS - API**
- Telematics-specific integrations: add the telematics API permission sets as needed

## Assign a permission set

1. Open **Users** in Business Central.
2. Open the user card.
3. In **User Permission Sets**, add a new line.
4. In **Permission Set**, select the required Shipper TMS permission set.
5. Repeat for any additional roles the user needs.

## Verify

Use these quick checks:

- Planner: search for **Transport Requests**
- Administrator: search for **Shipper TMS Setup**
- API account: test the relevant API endpoint

If the page or API is accessible, the permission set is assigned correctly.

## Related

- [Installation](installation.md)
- [Buy licenses](buylicenses.md)
- [TMS Setup](setup.md)
