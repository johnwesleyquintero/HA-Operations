---
document: spreadsheet-registry.md
purpose: Inventory of HA operational spreadsheets and workbook metadata
owner: Wesley Quintero
maintained_by: Wesley Quintero
last_reviewed: 2026-11-28
confidentiality: Internal operational context
---

# HA Spreadsheet & Workbook Registry

> **Purpose:** A metadata-first catalog of operational Google Sheets and workbooks. Use this registry to identify the right source, understand its purpose and ownership, and decide which workbook is relevant before opening or importing sheet data. This avoids importing multiple protected or tab-locked workbooks merely to build a filter or determine where information belongs.

**Last reviewed:** 2026-11-28  
**Registry owner:** Wesley Quintero  
**Spreadsheet creator / builder:** Recorded per workbook; creator is not necessarily the current owner or approver.

## How to use this registry

1. Start here when locating a workbook, filtering candidate sources, or orienting an AI assistant.
2. Use the workbook name, status, purpose, type, owner, update cadence, data-entry method, and downstream dependencies to select the relevant source.
3. Open or import only the selected workbook and only the tabs/ranges needed for the task. Do not import every workbook by default.
4. For protected or tab-locked workbooks, use the authorized creator/assistant workflow where directed. A listed URL does not prove that a person or assistant has access.
5. Use the **Nox access check** field for Nox to record verified access or limitations. Do not assume access from a prefilled row or successful link resolution.
6. Confirm live values in the source workbook before making operational decisions. This registry describes systems; it is not a live inventory, shipment, quote, or performance data source.

## Ownership and approval controls

- **Owner** means the person accountable for the operational workbook; **Creator** means who originally built it. Keep these separate.
- Nox may create, maintain, or help update spreadsheets when assigned, but that does not make Nox the business owner or decision-maker.
- Wesley coordinates operational use, validates data and changes, and maintains this registry.
- Justin retains management review and approval authority where a decision or approval is required.
- A workbook marked **Draft**, **Proposed**, or described as awaiting review must not be treated as approved or as having replaced an existing source of truth.
- Preserve existing formulas, protected ranges, historical records, and workbook structure. Make minimal, auditable changes and verify the result.
- When a new workbook replaces an old one, record the approval and migration explicitly before changing the old workbook's status to Archived.

## Workbook inventory

### Active workbooks

| Sheet name | Status | Link | Type | Purpose | Owner | Creator | Update cadence | Data entry | Feeds into / dependencies | Notes / gaps | Last reviewed | Nox access check |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| HA Inventory Plan | Active | [Open workbook](https://docs.google.com/spreadsheets/d/1pzVXLu4Woje4T-nETeaNULH0pPAdaMJ1infnsxzyy7E/edit) | Planning | Inventory plan with the order planner: demand through Dec 2028 tied to actuals, planned orders by product and country, PO schedule and cash totals, container fit. Replaces the Justin draft. | Justin (to confirm) | Nox | Not specified | Not specified | Not specified | Ownership to confirm. | Not recorded | Not checked |
| HA Shipping Tracker | Active | [Open workbook](https://docs.google.com/spreadsheets/d/1iqosUhiFcrUh_x-m3VFR0-5P4VqzjDP1HlKuD4kKHq8/edit) | Tracking | Every PO from PI to arrival and every send after it (AWD, 3PL, FBA, Walmart, TikTok) in one place. Status, Days late and Next step are calculated from dates; Dashboard shows what is late and what arrives next; Checks lists what to update. One Replenishment Log replaces the four send tabs. | Wesley | Nox | As it happens (each PO step and each send) | Typed by Wesley | HA Inventory Plan (POs tab, read live since Oct 15) and Reporting Hub Ops Log inbound columns through the Plan; Nox morning brief still reads the Inventory / Shipping Tracker until the switch. | Draft for Wesley to review; it does not replace the Inventory / Shipping Tracker until Wesley and Justin approve. | Not recorded | Not checked |
| Freight-Forwarder Outreach Tracker | Active | [Open workbook](https://docs.google.com/spreadsheets/d/1N7CUsI7kl3wsb8-iqFYdl0ojuXTCrWErYotEZH07__c/edit?gid=0#gid=0) | Tracking | Track freight forwarder outreach, communications, quotations, rates, service options, and follow-ups. Compare forwarder quotes and costs to support China-to-US/CA/UK routing and shipping decisions. | Wesley | Wesley (Drive owner) | As needed | Typed by hand | Not specified | Not specified | Not recorded | Not checked |
| HA Shipment Logistics Comparison | Active | [Open workbook](https://docs.google.com/spreadsheets/d/1kHKgk26CfQT1QtTZmA09Qf7l5dMD5mijonewIB6E1Ug/edit) | Planning | Per-shipment decision tool for the 2027 logistics plan: compares total cost through the Amazon path (AGL > AWD) and third-party freight quotes (EXW, FOB or DDP; FCL, LCL or Air), with duty and tariff, delivery splits to AWD, FBA, Walmart and TikTok, cost by destination and product, and optional cost of capital. Compares shipping cost only, not product profitability. | Justin (to confirm) | Nox | As needed (each shipment) | Typed by hand (yellow cells) | 2027 logistics architecture decision (Justin, Nov 2026) | Draft built by Nox from the 2027 Logistics Strategy document; seeded AWD rates need verification. | Not recorded | Not checked |
| HA Listing Change Calendar (A/B tests, seasonal rotations, update projects) | Active | [Open workbook](https://docs.google.com/spreadsheets/d/1L5jMrKAYBrO1Q6lrg1fdAKKjkiDS3jgxw6F9STgmD7g/edit) | Planning | Plan and log listing changes: A/B tests, seasonal hero-image rotations and update projects (first item: Compact A+ drawer image). Includes a project queue, seasonal search and purchase data, a change log of price/coupon/listing changes and a before/after readout. | Wesley (to confirm) | Nox | Weekly | Typed by hand (yellow cells) | L10 A/B row, R2 rock, Monday A/B report | Draft built by Nox; dates are suggestions for the team to adjust. | Not recorded | Not checked |

### Archived workbooks

| Sheet name | Status | Link | Type | Purpose | Owner | Creator | Update cadence | Data entry | Feeds into / dependencies | Notes / gaps | Last reviewed | Nox access check |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Inventory / Shipping Tracker | Archived | [Open workbook](https://docs.google.com/spreadsheets/d/1alqu8L-GG6iGDq4g2fDFpntWdwqJZP1D1-9seolZghw/edit) | Tracking | Purchase orders, production, shipping and balance payments by product and market. | Wesley | Justin | Weekly | Typed by hand | Nox morning brief; weekly planning | Retained as historical reference. HA Shipping Tracker is a draft replacement and must not be treated as approved until Wesley and Justin approve. | Not recorded | Not checked |
| HA Inventory Forecast | Archived | [Open workbook](https://docs.google.com/spreadsheets/d/1VDsb5YnaFRYXZH4PcCz8OOfJ_HI7bXvBOW6KOvaH4lw/edit?gid=1657418782#gid=1657418782) | Planning | Inventory forecast by product and marketplace (Amazon US/CA/GB, TikTok, Walmart, Shopify) with POs, inputs, dashboard and executive summary. | Justin | Justin | Monthly | Typed by hand | Forecast summary exported into HA Stock and Supply Planning. | Archived; historical source. | Not recorded | Not checked |
| HA Stock and Supply Planning | Archived | [Open workbook](https://docs.google.com/spreadsheets/d/1RUxG51a6fdzu5Bfey0Dz_-A20jz60dCU/edit?gid=505666025#gid=505666025) | Planning | Stock and supply planning (Excel file in the shared drive). | Wesley (to confirm) | Justin | Not specified | Not specified | Not specified | Ownership to confirm. | Not recorded | Not checked |
| HA Inventory Plan (DRAFT for Justin review) | Archived | [Open workbook](https://docs.google.com/spreadsheets/d/1M4GdgMAspuihSvR1W-g_Rw7JUk8JKbTFMzEKWcJFDUo/edit) | Planning | Rebuilt demand forecast and supply plan: demand by marketplace and SKU, supply and POs, stock snapshot, suggested POs, AWD vs FBA, and comparison of forecast with actual units. | Justin (to confirm) | Nox | Not specified | Not specified | Not specified | Draft for Justin to review; it does not replace HA Inventory Forecast or HA Stock and Supply Planning until approved. | Not recorded | Not checked |

### Proposed review workbooks

| Sheet name | Status | Link | Type | Purpose / description | Owner | Creator | Update cadence | Data entry | Feeds into | Notes / gaps | Last reviewed | Nox access check |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| DRAFT - HA Shipment Logistics Comparison - Scenario 3 Suaid quote (Nov 25 2026) | Proposed | [Open workbook](https://docs.google.com/spreadsheets/d/1XeTUyINgxk7ZdoYtzGH3FGNO6EitruOCCqwZN5NLrTg/edit?gid=695136029#gid=695136029) | Not specified | Logistics Forwarder Comparison. | Wesley | Nox | Daily | Mixed | R6 | Awaiting review; proposal only. | Not recorded | Not checked |
| DRAFT - 3PL Rate Comparison (Nov 20 2026) | Proposed | [Open workbook](https://docs.google.com/spreadsheets/d/1WfpHY_IG1zeGD6EYDSyI3v7sPcmPTRse7Iw5wNQScog/edit?gid=0#gid=0) | Not specified | Logistics 3PL Rate Cards Comparison. | Wesley | Nox | Daily | Mixed | R6 | Awaiting review; proposal only. | Not recorded | Not checked |
| DRAFT - HA Listing Change Calendar - A/B Initial Results (Nov 25 2026) | Proposed | [Open workbook](https://docs.google.com/spreadsheets/d/1HGCCt_msw4cvqeKJvascxlaLL_mIUTgoGIcP1MMnTYE/edit?gid=1888945978#gid=1888945978) | Not specified | HA Listing Change Calendar with A/B Initial Results. | Wesley | Nox | Daily | Mixed | R2 | Awaiting review; proposal only. | Not recorded | Not checked |

## Maintenance

- Update this registry when a workbook is created, materially repurposed, approved as a replacement, archived, or when its owner / creator / access status changes.
- Keep descriptions at the metadata level. Do not copy live rows, inventory quantities, shipment statuses, quotes, formulas, or sensitive tab contents into this catalog.
- Record only verified access results in **Nox access check** (for example: accessible, blocked by permission, specific tabs unavailable, or access not tested), with a check date and brief evidence where useful.
- If workbook ownership or approval is unclear, retain **to confirm** rather than guessing.
- Keep draft/proposed and archived workbooks visible so historical dependencies and migration status remain understandable.
