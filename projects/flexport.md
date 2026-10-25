# Flexport Quote — R6 Logistics Optimization

**Last reviewed:** October 25, 2026  
**Purpose:** Preserve Flexport's quote details and document whether the quote can be entered into the HA Shipment Logistics Comparison workbook.

## 1. Quote Summary

| Field | Quote detail |
|---|---|
| Forwarder | Flexport |
| Shipment ID | `FLEX-4278038` |
| Quote ID | `Quote-5822794` |
| Status | Pending approval when issued; **expired October 15, 2026** |
| Incoterm | FOB |
| Mode | Ocean FCL |
| Equipment | 2 × 40' HQ containers |
| Pickup | Shenzhen, China |
| Port of loading | Yantian, China |
| Port of arrival | Los Angeles, California, USA |
| Final AWD delivery | **Not confirmed in the quote details provided** |
| Customs brokerage | Declined |
| Insurance | Included (per shipment) |
| Carbon offset | Included |
| Transit estimate | Likely 25 days; latest estimate 33 days; carrier estimate 22–29 days |
| Weight / volume | Not populated in the quote details provided |

**Important:** The quote has expired. Request a refreshed quote before treating the price as current or making a booking decision.

## 2. Itemized Charges

| Charge | Calculation | Amount |
|---|---:|---:|
| FCL — 40' HQ | $8,350 × 2 | $16,700.00 |
| AMS | Flat charge | $35.00 |
| ISPS | $15 × 2 | $30.00 |
| Booking fee | Flat charge | $85.00 |
| Document turnover | Flat charge | $65.00 |
| Import handling | Flat charge | $75.00 |
| Carbon offset | $13.45 × 2 metric tonnes CO₂e | $32.13 |
| **Quoted total** |  | **$17,022.13** |

Flexport notes that final charges may change based on actual weight/volume, general rate increases (GRIs), and other applicable accessorials or charges. The quote does not establish that every cost required to deliver the cargo to the final AWD facility is included.

## 3. Workbook Readiness

**Assessment: Partially ready for data entry; not ready for a verified apples-to-apples cost comparison.**

The quote is detailed enough to enter the known Flexport fields into the `HA Shipment Logistics Comparison (DRAFT).xlsx` workbook, provided the record is marked **expired / refresh required** and all unverified costs remain blank or explicitly pending—not zero.

### Fields that can be entered now

- Forwarder: Flexport
- Quote reference: `Quote-5822794`
- Shipment reference: `FLEX-4278038`
- Mode: Ocean FCL
- Equipment: 2 × 40' HQ
- Pickup / origin: Shenzhen, China
- Port of loading: Yantian, China
- Port of arrival: Los Angeles, California, USA
- Incoterm: FOB
- Ocean FCL charge: $16,700.00
- Itemized additional quoted charges: $322.13
- Quoted total: $17,022.13
- Insurance: Included
- Carbon offset: Included
- U.S. customs brokerage: Declined
- Transit estimate: Record the 22–29 day carrier estimate and note the separate 25-day likely / 33-day latest estimates
- Quote validity: Expired October 15, 2026; refresh required

### Inputs still needed before the workbook can support a decision

- **Refreshed Flexport quote** with current price and validity.
- **Final AWD delivery:** exact AWD facility/address and confirmation of trucking/final-mile charges, delivery/appointment service, and any exclusions.
- **Customs and import costs:** obtain a comparable brokerage quote and clarify duties, taxes, entry fees, and destination charges. Customs brokerage is explicitly declined in this quote; do not assume it is included.
- **Cargo data:** actual gross weight, CBM, carton dimensions, carton count, and confirmation of the cargo/equipment assumptions. Weight and volume are blank in the quote details.
- **Comparable Amazon/AGL baseline:** final invoice or itemized freight bill and confirmation of what the amount includes. The Amazon AWD amount currently located is an estimate, not a verified final freight cost, and the shipment has not been independently confirmed as AGL-arranged.
- **Quantity reconciliation:** Amazon AWD record shows 11,796 units, while the current RFQ notes show 11,808 units (Classic Food Mill 5,808 + Compact Food Mill 6,000). Resolve the 12-unit discrepancy and confirm both records represent the same cargo.
- **Workbook setup:** replace the sample-like allocation in `Shipment Setup` with confirmed instructions before using calculated outputs. Confirm carton, unit-cost, duty/HTS, and rate-card inputs; missing inputs must not be interpreted as zero cost.

### Recommended entry and validation approach

1. Enter only the known quote fields and itemized charges.
2. Mark quote status as expired / refresh required.
3. Leave unknown costs blank or label them pending; do not force unknowns to zero.
4. Check that the workbook's line items total $17,022.13 without double-counting included services.
5. Refresh the quote and request an itemized, comparable scope through the exact AWD facility.
6. Normalize the Flexport scope against the verified Amazon/AGL final cost before calculating savings or recommending a route.

## 4. Preliminary Headline Comparison — Not Decision-Ready

| Reference | Amount | Qualification |
|---|---:|---|
| Amazon AWD shipment record | $14,395.67 | Estimated shipping fees; final cost and inclusions unverified |
| Flexport quote | $17,022.13 | Expired quote; customs brokerage declined; final AWD delivery not confirmed |
| Apparent difference | $2,626.46 | Flexport figure is 18.24% higher than the Amazon estimate, **but this is not a verified like-for-like cost difference** |

Do not present the $2,626.46 difference as confirmed additional cost or savings. The quote scopes, final charges, cargo quantity, and Amazon/AGL booking identity remain unresolved.

## 5. Next Actions

- [ ] Request a refreshed Flexport quote.
- [ ] Confirm all-in delivery to the designated AWD facility and itemize exclusions.
- [ ] Obtain a comparable customs-brokerage/import-cost estimate.
- [ ] Confirm shipment weight, CBM, carton data, and quantity.
- [ ] Request the historical Amazon/AGL booking confirmation and final freight invoice/billing detail.
- [ ] Populate and validate the workbook using confirmed inputs only.

**Bottom line:** The Flexport quote can populate the workbook's known quote fields now, but it is not current and is not yet sufficient for a final cost comparison or routing recommendation.
