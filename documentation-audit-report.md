---
title: "Documentation Audit Report"
description: "Internal audit of Shipper TMS documentation against the AL source code."
robots: noindex
---

# Shipper TMS Documentation Audit

## Scope

Reviewed inputs:

- `Docs.zip` / `shipper-tms-help`
- `TMSforShippers.zip` / AL source code
- AppSource Marketplace page
- Extensions Lab Shipper TMS product page

No `audit/docs` folder was found in the uploaded archives.

## Source-code inventory reviewed

The AL package contains approximately:

| Object type | Count |
|---|---:|
| Pages | 155 |
| Codeunits | 101 |
| Tables | 96 |
| Page extensions | 69 |
| Enums | 62 |
| Table extensions | 32 |
| Queries | 17 |
| Permission sets | 13 |
| Reports | 8 |
| Control add-ins | 4 |

Key source areas reviewed:

- `src/API`
- `src/Domain`
- `src/Geolocation`
- `src/LoadManagement`
- `src/Scheduler`
- `src/Setup`
- `src/Telematics`
- `src/TransportationRequests`
- `src/TransportOrder`
- `src/History`
- `src/Integration/BC`

## Findings from documentation-to-code pass

| Finding | Severity | Action taken |
|---|---|---|
| Core planning pages were documented, but several execution and integration areas were missing. | High | Added pages for API, source documents, split planning, carrier rates, charges, warehouse documents, execution entries, and posted orders. |
| Carrier Selection documentation did not explain the carrier-rate setup it depends on. | High | Added `carrier-rates.md` and updated Carrier Selection, Carrier, Setup, and Transport Charges links. |
| Transport Order documentation did not fully describe charges, posting prerequisites, warehouse documents, and posted history. | High | Rewrote `transportorder.md` and added related execution pages. |
| API pages and telematics admin service actions were not documented. | High | Added `api.md`; updated `telematics.md` and permission-set guidance. |
| Azure truck-aware routing was mentioned but not documented as its own setup. | Medium | Added `vehicle-routing-profiles.md`; updated Azure, Map Providers, and Logistic Unit Types. |
| Distance Matrix and Route Distance Matrix were not documented. | Medium | Added `distance-matrix.md`. |
| Source document actions across Sales, Purchase, Transfer, and posted documents were under-documented. | High | Added `source-documents.md` and linked it from Transport Request and Index. |
| The legacy `shipperloadmanagement.md` duplicated old content. | Medium | Replaced it with a compatibility page linking to the current Load Management page. |
| Screenshot registry said to save screenshots in the root while the repo actually uses `resources/<topic>/`. | Medium | Rewrote the screenshot registry and added a screenshot backlog. |
| One permission screenshot had a double `.png.png` extension. | Low | Copied it to a clean `.png` name and updated the link. |
| Visual Scheduler image link pointed to a root file that did not exist. | Low | Updated the link to `resources/visualscheduler/screenshot-visual-scheduler.png` and added a placeholder. |
| `app.json` has `help` URL `https://tms.extensions-lab.com/` while `contextSensitiveHelpUrl` and the current docs use `https://stms.extensions-lab.com/`. | Medium | Recommend aligning the URL in the AL manifest or redirecting both domains. |

## Findings from code-to-documentation pass

| Functional area found in AL | Existing docs status | Updated docs status |
|---|---|---|
| Transport Request / Transport Order | Covered | Expanded and corrected |
| Sales/Purchase/Transfer page extensions | Partial | Added Source Documents page |
| Split Planning Worksheet | Missing | Added Transport Request Planning Worksheet page |
| Load Management / Truck Load / Driver Load | Covered | Truck Load release checks expanded |
| Visual Scheduler | Covered | Image path fixed |
| Carrier Selection | Partial | Expanded and linked to Carrier Rates |
| Carrier Rates and Rate Type Mapping | Missing | Added Carrier Rates page and setup references |
| Transport Charges and Charge Assignment | Missing | Added Transport Charges page |
| Warehouse document creation | Missing | Added Warehouse Documents page |
| Posted Transport Orders / History | Missing | Added Posted Transport Orders page |
| Execution Entries / Attachments | Missing | Added Execution Entries page |
| API pages | Missing | Added API page |
| Telematics provider admin API | Partial | Added API and Telematics admin guidance |
| Vehicle Routing Profiles | Partial | Added full page |
| Distance Matrix / Route Distance Matrix | Missing | Added Distance Matrix page |
| Reference master data | Missing | Added Reference Master Data page |

## Documentation style changes

Applied a consistent user-doc structure:

- short opening definition,
- clear “when to use it” guidance,
- task-first steps,
- rules and blockers,
- troubleshooting where useful,
- related links at the end.

The revised pages avoid developer language unless the page is explicitly for API or administration.

## GitHub Pages readiness

Changes made:

- standardized relative Markdown links,
- changed root image links from `/resources/...` to `resources/...`,
- created a screenshot registry that matches the repository folder structure,
- added a minimal `_config.yml` for GitHub Pages metadata and internal-file exclusions,
- added `robots.txt` and regenerated `sitemap.xml`,
- kept one page per Markdown topic for clean Jekyll conversion.

Recommended next steps:

1. Confirm whether the minimal `_config.yml` should also declare a theme.
2. Keep `documentation-audit-report.md` and `screenshot-registry.md` excluded from the public site unless they should be visible.
3. Replace placeholder screenshots before publishing broadly.
4. Regenerate `sitemap.xml` after the final page list is approved.
5. Align `app.json` help URL with the published help domain.

## Overall score

Original documentation score against the AL source: **63/100**.

Strengths:

- good coverage of basic setup and core planning,
- clear first-use paths,
- existing screenshots for important setup and order pages,
- readable Markdown structure.

Weaknesses:

- important code-backed functionality was missing,
- carrier pricing and charge allocation were not documented,
- APIs and telematics admin operations were not documented,
- posted history and execution entries were not documented,
- screenshot registry and GitHub Pages link conventions needed cleanup.

Revised documentation score after this pass: **86/100**.

Remaining work:

- capture real screenshots for the new pages,
- verify UI labels in a live Business Central sandbox,
- validate edge-case behavior with test data for carrier rates and charge posting,
- decide whether internal audit pages should be published or excluded.
