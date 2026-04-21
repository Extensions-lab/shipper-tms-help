---
title: "Screenshot Registry"
description: "Internal authoring registry for screenshots used in the Shipper TMS documentation set."
---

# Screenshot registry

This file is for documentation maintenance.

## Save location

Save every screenshot as a **PNG** file directly in the `docs/` root folder.

Do not create subfolders for these screenshots unless you also update the links in the Markdown files.

Target location for every file below:

- `docs/<filename>.png`

## Capture rules

- Use Business Central in English.
- Use a clean demo company or sanitized customer data.
- Avoid personal data, email addresses, phone numbers, or real vehicle registrations unless they are fake/demo values.
- Use the standard light theme.
- Capture the main working area only. Avoid browser tabs, bookmarks, and desktop clutter.
- Keep the UI readable at normal zoom.
- If a page has filters, set realistic values before taking the screenshot.

## Existing repo images already reused

The following pages already use images that exist in `docs/resources`, so you do **not** need to create new screenshots for them unless you want to replace them with fresher UI captures:

- `index.md`
- `installation.md`
- `buylicenses.md`
- `setup.md`
- `googlemapintegration.md`
- `maplocation.md`
- `transportrequest.md`
- `transportorder.md`

## Screenshots still needed

| File name | Used in | What to capture |
|---|---|---|
| `screenshot-permissions-user-permission-sets.png` | `assignpermissionsets.md` | User card in Business Central with the current Shipper TMS permission-set names visible |
| `screenshot-map-providers-setup.png` | `mapproviders.md` | The **Map Provider Settings** section in Shipper TMS Setup |
| `screenshot-azure-maps-subscription-key.png` | `azuremapsintegration.md` | The part of setup where **Azure Maps Subscription Key** and **Azure Maps Geo Scope** are visible |
| `screenshot-load-management.png` | `loadmanagement.md` | The Load Management page showing both the pending request pool and planning tree |
| `screenshot-truck-load-management.png` | `truckloadmanagement.md` | Truck Load Management with truck slots in the upper section and candidates in the lower section |
| `screenshot-driver-load-management.png` | `driverloadmanagement.md` | Driver Load Management showing driver slots and status/conflict columns |
| `screenshot-visual-scheduler.png` | `visualscheduler.md` | Visual Scheduler timeline with grouped requests and at least one Transport Order frame |
| `screenshot-telematics-setup-card.png` | `telematics.md` | Telematics Setup card showing connection fields and sync actions |

## Suggested capture notes by file

### `screenshot-load-management.png`

Make sure both sections are visible:

- **Pending Transport Requests**
- **Transport Order Planning**

### `screenshot-truck-load-management.png`

Make sure these are visible:

- truck slot rows,
- **Load %**,
- current status,
- candidate list in the lower section.

### `screenshot-driver-load-management.png`

Make sure these are visible:

- driver slot rows,
- assigned vehicle,
- **Next Step**,
- conflict columns if possible.

### `screenshot-visual-scheduler.png`

Capture a period where:

- several requests are visible,
- at least one Transport Order frame is visible,
- the grouping label is obvious.

### `screenshot-telematics-setup-card.png`

Capture the card with:

- provider,
- authentication fields,
- sync fields,
- **Manage Secrets** or **Full Sync** in the action bar if possible.
