# Screenshot Registry for Shipper TMS Documentation

Use this registry to create and maintain screenshots for GitHub Pages documentation.

## Screenshot rules

- Save screenshots as `.png`.
- Use lowercase kebab-case file names.
- Store files under `docs/resources/<topic>/`.
- Use the exact relative Markdown links shown below.
- Use demo data only.
- Mask or remove API keys, secrets, access tokens, customer-sensitive names, phone numbers, driver private data, and vehicle registration numbers.
- Capture Business Central at 100% browser zoom where possible.
- Prefer 16:9 screenshots around 1600×900 or 1920×1080.
- Crop only when it makes the UI easier to read.
- Do not add arrows or red boxes unless the screenshot would otherwise be confusing.
- Every screenshot must have meaningful alt text.

---

## Registry

| Priority | Target page | Insert after section | Markdown image link to insert | Save as | What to capture | How to capture |
|---|---|---|---|---|---|---|
| P0 | `carrier-rate-type-mapping.md` | Before “Create a mapping” | `![Carrier Rate Type Mapping list](resources/carrier-rate-type-mapping/screenshot-carrier-rate-type-mapping-list.png)` | `docs/resources/carrier-rate-type-mapping/screenshot-carrier-rate-type-mapping-list.png` | Carrier Rate Type Mapping list with 3–5 example rows | Open Carrier Rate Type Mapping in Business Central; show Rate Type, Item Charge No., Description. |
| P0 | `carrier-rates.md` | Geographic matching section | `![Carrier Rate geographic fields](resources/carrier-rates/screenshot-carrier-rate-geographic-fields.png)` | `docs/resources/carrier-rates/screenshot-carrier-rate-geographic-fields.png` | Carrier Rate card/list showing country, county, city, post code fields | Use one carrier rate example; do not imply Region Code is used unless code is changed. |
| P0 | `api.md` | Attachment upload rules | `![Attachment upload API example](resources/api/screenshot-api-attachment-upload-postman.png)` | `docs/resources/api/screenshot-api-attachment-upload-postman.png` | Postman or API client request for upload attachment | Mask tenant/company/API host/token. Show MIME type, base64 field shortened, expected response. |
| P1 | `setup.md` | Check setup readiness | `![TMS Setup readiness check result](resources/setup/screenshot-tms-setup-readiness-check.png)` | `docs/resources/setup/screenshot-tms-setup-readiness-check.png` | Result message after choosing Check TMS Settings | Capture one “passed” or “blocking issues” result. Prefer blocking issues if troubleshooting section uses it. |
| P1 | `setup.md` | Carrier Selection setup | `![Carrier Selection settings in TMS Setup](resources/setup/screenshot-tms-setup-carrier-selection-settings.png)` | `docs/resources/setup/screenshot-tms-setup-carrier-selection-settings.png` | TMS Setup Carrier Selection group | Show Carrier Selection Enabled, Auto Create Charge Line, Auto Create Item Charge, Carrier Rate Types Mapping action if visible. |
| P1 | `source-documents.md` | Create transport demand | `![Create Transport Request action on Sales Order](resources/source-documents/screenshot-sales-order-create-transport-request-action.png)` | `docs/resources/source-documents/screenshot-sales-order-create-transport-request-action.png` | Sales Order page action group with Create Transport Request | Use demo Sales Order with releasable lines. |
| P1 | `transportrequest.md` | After creating a request | `![Transport Request created from source document](resources/transportrequest/screenshot-transport-request-after-source-document.png)` | `docs/resources/transportrequest/screenshot-transport-request-after-source-document.png` | Transport Request card/list after source document generation | Show source document reference, load/unload locations, planned dates, status. |
| P1 | `transport-request-planning.md` | Split example | `![Transport Request Planning split lines](resources/transport-request-planning/screenshot-transport-request-planning-split-lines.png)` | `docs/resources/transport-request-planning/screenshot-transport-request-planning-split-lines.png` | Planning page where one source line is split into multiple transport requests | Show original quantity and split quantities. |
| P1 | `loadmanagement.md` | Assign requests to a load | `![Load Management request assignment](resources/loadmanagement/screenshot-load-management-assign-requests.png)` | `docs/resources/loadmanagement/screenshot-load-management-assign-requests.png` | Load Management worksheet with selected released requests and load/order area | Capture before choosing Assign/Create Load. |
| P1 | `truckloadmanagement.md` | Slot status legend | `![Truck Load Management slot statuses](resources/truckloadmanagement/screenshot-truck-slot-status-legend.png)` | `docs/resources/truckloadmanagement/screenshot-truck-slot-status-legend.png` | Truck Load Management showing several slot statuses | Include empty/planned/full/overloaded/released/conflict if possible. |
| P1 | `truckloadmanagement.md` | Candidate reasons | `![Truck Load Management candidate reasons](resources/truckloadmanagement/screenshot-truck-load-candidate-reasons.png)` | `docs/resources/truckloadmanagement/screenshot-truck-load-candidate-reasons.png` | Candidate list for selected truck slot | Show eligible/warning/blocked or reasons columns. |
| P1 | `vehicle-compartments-and-transportation-conditions.md` | How planners see the result | `![Compartment assignment for truck load](resources/truckloadmanagement/screenshot-truck-load-compartment-assignment.png)` | `docs/resources/truckloadmanagement/screenshot-truck-load-compartment-assignment.png` | Transport requests assigned to compartments | Use a load where requests are grouped under a visible compartment. |
| P1 | `driverloadmanagement.md` | Driver conflicts | `![Driver conflict details](resources/driverloadmanagement/screenshot-driver-conflict-details.png)` | `docs/resources/driverloadmanagement/screenshot-driver-conflict-details.png` | Driver Load Management or conflict details page | Show double booking or unavailable driver example. |
| P1 | `visualscheduler.md` | Visual timeline | `![Visual Scheduler timeline](resources/visualscheduler/screenshot-visual-scheduler-timeline.png)` | `docs/resources/visualscheduler/screenshot-visual-scheduler-timeline.png` | Scheduler timeline with requests/orders grouped by route/driver/vehicle | Capture a clean planning week with several bars. |
| P1 | `transportorder.md` | Transport Order overview | `![Transport Order with route and assignments](resources/transportorder/screenshot-transport-order-route-assignments.png)` | `docs/resources/transportorder/screenshot-transport-order-route-assignments.png` | Transport Order card with carrier, vehicle, driver, route lines | Use demo data; no real driver/private data. |
| P1 | `transportorder.md` | Posting blockers | `![Transport Order posting blocker message](resources/transportorder/screenshot-transport-order-posting-blocker-message.png)` | `docs/resources/transportorder/screenshot-transport-order-posting-blocker-message.png` | Error/message shown when posting is blocked | Prefer a message involving unposted charge source documents or inactive source link. |
| P1 | `carrierselection.md` | Compare carrier options | `![Carrier Selection cost breakdown](resources/carrierselection/screenshot-carrier-selection-cost-breakdown.png)` | `docs/resources/carrierselection/screenshot-carrier-selection-cost-breakdown.png` | Carrier Selection page with several carriers and cost entries | Show selected carrier, rates/fees, total amount. |
| P1 | `transport-charges.md` | Allocation example | `![Transport charge allocation lines](resources/transport-charges/screenshot-transport-charge-allocation-lines.png)` | `docs/resources/transport-charges/screenshot-transport-charge-allocation-lines.png` | Charge assignment lines after allocation | Show allocation method and source document distribution. |
| P1 | `warehouse-documents.md` | Created warehouse document | `![Warehouse document created from Transport Order](resources/warehouse-documents/screenshot-warehouse-document-created-from-transport-order.png)` | `docs/resources/warehouse-documents/screenshot-warehouse-document-created-from-transport-order.png` | Warehouse Shipment/Receipt linked to Transport Order | Capture expected result after Create Warehouse Documents. |
| P2 | `reports.md` | Print documents | `![Transport Order report actions](resources/reports/screenshot-transport-order-report-actions.png)` | `docs/resources/reports/screenshot-transport-order-report-actions.png` | Report action menu on Transport Order | Show Loading Manifest, Packing List, Bill of Lading, Delivery Note, CMR Blank. |
| P2 | `execution-entries.md` | Attachment/proof | `![Execution Entry with attachment](resources/execution-entries/screenshot-execution-entry-with-attachment.png)` | `docs/resources/execution-entries/screenshot-execution-entry-with-attachment.png` | Execution Entry showing status/event and attachment | Use demo proof-of-delivery PDF/image. |
| P2 | `posted-transport-orders.md` | Posted history | `![Posted Transport Order history](resources/posted-transport-orders/screenshot-posted-transport-order-history.png)` | `docs/resources/posted-transport-orders/screenshot-posted-transport-order-history.png` | Posted Transport Order with lines/charges/history | Show read-only completed trip. |
| P2 | `mapproviders.md` | Provider setup | `![Map Provider setup](resources/mapproviders/screenshot-map-provider-setup.png)` | `docs/resources/mapproviders/screenshot-map-provider-setup.png` | Map provider settings | Mask keys. Show Google/Azure choice. |
| P2 | `maplocation.md` | Geocoded location | `![Map Location geocoding](resources/maplocation/screenshot-map-location-geocoding.png)` | `docs/resources/maplocation/screenshot-map-location-geocoding.png` | Map Location page with coordinates/map | Use demo address. |
| P2 | `vehicle-routing-profiles.md` | Azure truck profile | `![Vehicle Routing Profile settings](resources/vehicle-routing-profiles/screenshot-vehicle-routing-profile-settings.png)` | `docs/resources/vehicle-routing-profiles/screenshot-vehicle-routing-profile-settings.png` | Vehicle routing profile with height/weight/hazmat/toll settings | Use realistic but demo values. |
| P2 | `vehicle.md` | Vehicle compartments | `![Vehicle compartment setup](resources/vehicle/screenshot-vehicle-compartment-setup.png)` | `docs/resources/vehicle/screenshot-vehicle-compartment-setup.png` | Vehicle setup showing capacity and compartments/configuration | Use refrigerated/ambient example if possible. |
| P2 | `transportationconditions.md` | Condition compatibility | `![Transportation Conditions compatibility](resources/transportationconditions/screenshot-transportation-conditions-compatibility.png)` | `docs/resources/transportationconditions/screenshot-transportation-conditions-compatibility.png` | Transportation Conditions setup | Show frozen/ambient/chilled examples. |
| P1 | `telematics-setup.md` | Provider setup | `![Telematics provider setup](resources/telematics/screenshot-telematics-provider-setup.png)` | `docs/resources/telematics/screenshot-telematics-provider-setup.png` | Telematics setup page for one provider | Mask all credentials. |
| P1 | `telematics-provider-mapping.md` | Mapping | `![Telematics provider mapping](resources/telematics/screenshot-telematics-provider-mapping.png)` | `docs/resources/telematics/screenshot-telematics-provider-mapping.png` | Mapping between Business Central vehicles/drivers and provider entities | Use demo IDs. |
| P1 | `telematics-dispatch.md` | Dispatch log | `![Telematics dispatch log](resources/telematics/screenshot-telematics-dispatch-log.png)` | `docs/resources/telematics/screenshot-telematics-dispatch-log.png` | Dispatch log after publishing a Transport Order | Show status, provider, route/order reference, timestamp. |
| P2 | `telematics-sync-and-logs.md` | Inbound messages | `![Telematics inbound message log](resources/telematics/screenshot-telematics-inbound-message-log.png)` | `docs/resources/telematics/screenshot-telematics-inbound-message-log.png` | Inbound message/log page | Mask payload details if needed. |
| P2 | `usecase-salesorder-transportrequest.md` | First screenshot | `![Sales Order to Transport Request use case](resources/usecases/screenshot-usecase-sales-order-to-transport-request.png)` | `docs/resources/usecases/screenshot-usecase-sales-order-to-transport-request.png` | Before/after mini-flow from Sales Order to Transport Request | Use one simple Sales Order. |
| P2 | `usecase-create-first-transport-order.md` | First screenshot | `![First Transport Order use case](resources/usecases/screenshot-usecase-first-transport-order.png)` | `docs/resources/usecases/screenshot-usecase-first-transport-order.png` | Released request assigned to first Transport Order | Keep demo simple. |
| P2 | `usecase-complete-post-transport-order.md` | Posting result | `![Complete and post Transport Order use case](resources/usecases/screenshot-usecase-complete-post-transport-order.png)` | `docs/resources/usecases/screenshot-usecase-complete-post-transport-order.png` | Transport Order posted and opened as Posted Transport Order | Show expected final result. |

---

## Maintenance checklist

Before publishing a screenshot update:

- [ ] File name matches this registry.
- [ ] Image link in Markdown is relative and correct.
- [ ] Alt text explains the screenshot.
- [ ] No secrets or real customer data.
- [ ] Screenshot uses the same demo dataset naming conventions as other docs.
- [ ] Screenshot still matches the current Business Central UI and AL captions.
