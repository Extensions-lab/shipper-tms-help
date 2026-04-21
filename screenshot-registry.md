---
title: "Screenshot Registry"
description: "Internal authoring registry for screenshots used in the Shipper TMS documentation set."
---

# Screenshot registry

This file is for documentation maintenance.

## Save location

Save screenshots as **PNG** files under the matching topic folder:

- `resources/<topic>/<file-name>.png`

Do not save new screenshots in the documentation root.

## Capture rules

- Use Business Central in English.
- Use a clean demo company or sanitized customer data.
- Avoid personal data, email addresses, phone numbers, or real vehicle registrations unless they are fake demo values.
- Use the standard light theme.
- Capture the main working area only.
- Avoid browser tabs, bookmarks, and desktop clutter.
- Keep the UI readable at normal zoom.
- Do not expose API keys, access tokens, or telematics secrets.
- If a page has filters, set realistic values before taking the screenshot.

## Screenshot backlog

| File path | Used in | What to capture | Priority |
|---|---|---|---|
| `resources/source-documents/screenshot-source-document-actions.png` | `source-documents.md` | Released Sales Order or Transfer Order with the Shipper TMS action group visible | High |
| `resources/transport-request-planning/screenshot-transport-request-planning-worksheet.png` | `transport-request-planning.md` | Worksheet with Source Lines, Planned Transport Requests, and factbox visible | High |
| `resources/carrier-rates/screenshot-carrier-rates.png` | `carrier-rates.md` | Carrier Rates page with lane filters and pricing fields | High |
| `resources/carrierselection/screenshot-carrier-selection-results.png` | `carrierselection.md` | Carrier Selection results with at least two carriers and calculated amounts | High |
| `resources/transport-charges/screenshot-transport-charges.png` | `transport-charges.md` | Transport Order Charges section and the Show Assignment action | High |
| `resources/vehicle-routing-profiles/screenshot-vehicle-routing-profile-card.png` | `vehicle-routing-profiles.md` | Vehicle Routing Profile card with truck dimensions, weight, and avoid options | High |
| `resources/distance-matrix/screenshot-distance-matrix.png` | `distance-matrix.md` | Distance Matrix or Route Distance Matrix with Update Distance and Duration action | Medium |
| `resources/posted-transport-orders/screenshot-posted-transport-order.png` | `posted-transport-orders.md` | Posted Transport Order card with route lines and charges visible | Medium |
| `resources/execution-entries/screenshot-execution-entries.png` | `execution-entries.md` | Execution Entries page with status, timestamp, and attachment indicators | High |
| `resources/warehouse-documents/screenshot-warehouse-document-actions.png` | `warehouse-documents.md` | Released Transport Order showing Create Warehouse Documents and Show Warehouse actions | Medium |
| `resources/api/screenshot-api-overview.png` | `api.md` | Optional: sanitized API client, Business Central API page list, or integration diagram | Low |
| `resources/assignpermissionset/screenshot-permissions-user-permission-sets.png` | `assignpermissionsets.md` | User card with Shipper TMS permission sets visible | High |
| `resources/mapproviders/screenshot-map-providers-setup.png` | `mapproviders.md` | Map Provider Settings section in Shipper TMS Setup | High |
| `resources/azuremapsintegration/azure-maps-subscription-key.png` | `azuremapsintegration.md` | Azure Maps Subscription Key and Azure Maps Geo Scope, with key masked | High |
| `resources/loadmanagement/load-management.png` | `loadmanagement.md` | Load Management showing pending requests and planning tree | Medium |
| `resources/truckloadmanagement/truck-load-management.png` | `truckloadmanagement.md` | Truck Load Management with truck slots and candidate requests | Medium |
| `resources/driverloadmanagement/driver-load-management.png` | `driverloadmanagement.md` | Driver Load Management showing drivers, assigned vehicle, and conflict columns | Medium |
| `resources/visualscheduler/screenshot-visual-scheduler.png` | `visualscheduler.md` | Visual Scheduler timeline with at least one Transport Order frame | High |
| `resources/telematics/telematics-setup-card.png` | `telematics.md` | Telematics Setup card with provider, connection fields, and sync actions | Medium |

## Replacement workflow

1. Capture the screenshot.
2. Save it with the exact file path listed above.
3. Replace any placeholder image file.
4. Preview the Markdown page locally or in GitHub Pages.
5. Confirm that no secret values are visible.
