# Amazon Global Logistics (AGL) — Baseline Cost & Workbook Readiness

**Last reviewed:** October 25, 2026  
**Purpose:** Document the current evidence for the Amazon Global Logistics (AGL) baseline and list the exact information needed to complete the HA Shipment Logistics Comparison workbook.

## 1. Current Status

**Assessment: AGL baseline is blocked.** We have a historical Amazon AWD shipment record, a Bill of Lading (B/L), and a CBP Form 7501 reference, but we do not yet have a verified AGL booking confirmation or final itemized freight invoice/payment record.

Do not label the shipment as AGL-booked until the booking record confirms the freight arranger. Do not treat the Amazon AWD estimated shipping fee as a final AGL freight cost.

## 2. Shipment Evidence Located

| Field | Current evidence |
|---|---|
| Amazon AWD Shipment ID | `STAR-W3SYTEYFUNY3K` |
| Workflow ID | `wfcfe56fcb-05ca-454b-836e-4ea2a5ef1f51` |
| Workflow created | July 6, 2026 |
| Displayed shipping fee | **$14,395.67 — estimated**, not verified final cost |
| Cargo shown | 1,966 boxes; 1 SKU; 11,796 units |
| Ship-from supplier | Jieyang Fengxing Stainless Steel Products Co., Ltd. |
| Origin city / port | Yantian, China |
| Destination shown | IUTE, 16155 W Elwood St, Goodyear, AZ 85338 |
| Mode shown | Ocean |
| House B/L | `AMZDCN26JJJKW2GY` |
| Master B/L | `YMJAW226837921` |
| Customs broker file reference | `INL-12791577` |
| CBP Form 7501 | Located; total of approximately $24,239.12 relates to duties/taxes/fees, **not ocean freight** |

The B/L and customs entry help identify the shipment, but neither provides a usable itemized ocean-freight cost or independently proves AGL arranged the freight.

## 3. Exact Records Needed to Establish the AGL Baseline

Request access to the historical shipment's source records from Justin or the person who manages freight bookings, logistics, or accounts payable:

1. **AGL booking confirmation / shipment details** — confirms the forwarder, shipment identity, route, equipment, and services booked.
2. **Final AGL freight invoice or final billing statement** — actual billed freight and itemized charges, not an estimate.
3. **Itemized cost breakdown / billing export** — separates ocean freight, origin charges, destination charges, fuel or peak-season surcharges, handling, documentation, and other charges.
4. **Payment or settlement record** — shows what was actually paid and any outstanding balance, credits, or adjustments. A payment record supplements but does not replace the invoice.
5. **Amazon AWD fee detail** — confirms what the $14,395.67 estimate represents, whether it was finalized, and whether it includes final delivery, origin/destination handling, or other charges.
6. **Customs broker invoice and CBP entry detail** — keep customs brokerage, duties, taxes, and government fees separate from freight. The Form 7501 alone is not the freight invoice.
7. **Shipment-to-PO mapping** — identify the relevant PO and confirm the shipment matches the cargo being modeled.

Use the B/L references to locate the documents:
- House B/L: `AMZDCN26JJJKW2GY`
- Master B/L: `YMJAW226837921`
- Broker file: `INL-12791577`

The HA Shipping Tracker PO tab lists document/payment checklist fields such as BOL received, Entry summary, Shipping final bill, Balance 1 paid, and Balance 2 paid. Access to those underlying documents and payment records is still needed; the checklist alone is not enough.

## 4. Workbook Readiness Checklist

The workbook can be populated in stages. Unknown values must remain blank or explicitly marked **Pending**; never substitute zero for a missing cost.

### A. Shipment identity and cargo — required for both paths

- [ ] Confirm the PO and exact shipment being compared.
- [ ] Confirm product/SKU mix and actual units per SKU.
- [ ] Reconcile quantity: AWD record shows **11,796 units**; current RFQ notes show **11,808 units** (Classic Food Mill 5,808 + Compact Food Mill 6,000).
- [ ] Confirm carton count, cartons per SKU, carton dimensions, gross weight, and total CBM.
- [ ] Confirm container count/type (current RFQ: 2 × 40' HQ) and whether this matches the historical shipment.
- [ ] Confirm pickup location, port of loading, port of discharge, and exact final AWD facility/address.

### B. AGL / Amazon path — baseline-specific

- [ ] Verify AGL was the booking party using the booking confirmation or invoice.
- [ ] Obtain final invoice / billing statement and itemized charges.
- [ ] Confirm whether Amazon's $14,395.67 is still an estimate or a finalized amount.
- [ ] Map every charge to the workbook's cost categories without double-counting.
- [ ] Confirm included services and exclusions, especially origin charges, destination charges, final-mile AWD delivery, handling, and any accessorials.
- [ ] Add customs brokerage, duties/taxes, and government fees separately, using supporting records.
- [ ] Capture actual payment/credits/balance if total cost paid is part of the comparison.

### C. Flexport / alternative path — comparison-specific

- [ ] Obtain a refreshed Flexport quote; current quote `Quote-5822794` expired October 15, 2026.
- [ ] Confirm final AWD delivery to the same facility and itemize trucking, destination charges, appointments, and exclusions.
- [ ] Obtain a comparable customs-brokerage/import-cost estimate; the Flexport quote says customs brokerage is declined.
- [ ] Confirm quote validity, cargo dimensions/weight/CBM, and whether rates may change with GRI or accessorials.
- [ ] Collect at least one other alternative quote (e.g., FCLGO or Tactical) if the milestone requires multi-forwarder coverage.

### D. Workbook configuration and validation

- [ ] Clear or replace the sample-like allocation in `Shipment Setup` with confirmed shipment instructions.
- [ ] Verify unit COGS and SKU mix if the workbook uses them in landed-cost or per-unit calculations.
- [ ] Confirm HTS classification, duty/tariff assumptions, and applicable rates with the broker; do not guess.
- [ ] Verify each rate-card value, currency, effective date, service scope, and source.
- [ ] Check whether quote totals reconcile to their itemized lines.
- [ ] Confirm DDP/FOB responsibilities and exclusions so costs are neither double-counted nor omitted.
- [ ] Compare like-for-like route, equipment, cargo, destination, service level, and included costs.
- [ ] Review formula/check tabs for missing inputs or suspicious zero outputs.
- [ ] Keep evidence/source references and mark each field as Confirmed, Estimated, or Pending.

## 5. Minimum Viable Completion Order

To avoid unnecessary digging, complete the workbook in this order:

1. **Confirm the shipment and cargo.** Resolve the 12-unit mismatch and obtain carton/weight/CBM data.
2. **Request the AGL evidence packet.** Ask for the booking confirmation, final itemized invoice, AWD fee detail, and payment record for the B/L references above.
3. **Refresh Flexport.** Ask for a current quote covering delivery to the same AWD facility and get customs brokerage priced separately.
4. **Enter verified quote lines.** Populate known fields and mark gaps Pending; do not invent costs.
5. **Normalize and validate.** Reconcile the itemized totals, confirm service inclusions/exclusions, and compare the same shipment scope.
6. **Only then calculate the cost difference.** Treat the current $14,395.67 Amazon figure as an estimate until its final status and inclusions are verified.

## 6. Current Comparison Guardrail

The current headline figures are:
- Amazon AWD displayed estimate: **$14,395.67**
- Flexport expired quote: **$17,022.13**
- Apparent difference: **$2,626.46**, with Flexport's quote 18.24% higher than the Amazon estimate.

This is **not a verified like-for-like result**. The Amazon figure's final amount and inclusions are unverified; Flexport's quote is expired, customs brokerage is declined, final AWD delivery is unconfirmed, and cargo quantities differ by 12 units. Do not report this as confirmed extra cost or savings.

**Bottom line:** The next blocker is access to the actual historical AGL booking and final cost records—not more browsing of the same AWD screen. Request the source documents, then finish the workbook with verified, comparable inputs.
