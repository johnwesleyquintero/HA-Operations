# Flexport — Freight Quote & 3PL Pricing Reference

**Provider:** Flexport  
**Primary contact:** Jordan Politi, Enterprise Solutions  
**Email:** jpoliti@flexport.com  
**Record updated:** November 20, 2026  
**Purpose:** Preserve the freight quote details, general 2026 3PL rate-card information, and the current Scenario 2 workbook model in one place without mixing confirmed provider pricing with internal assumptions.

> **Status:** Partial pricing reference only. The historical freight quote expired on October 15, 2026. The 2026 3PL rate sheet is general/non-binding and does not include all destination-specific or service-specific costs. The workbook scenario is a model, not a current executable Flexport quote.

## 1. Source records

### A. Historical FCL freight quote

| Field | Recorded value |
|---|---|
| Provider | Flexport |
| Quote reference | Quote-5822787 |
| Quote validity | Through October 15, 2026 — **expired** |
| Incoterm | FOB |
| Mode | FCL |
| Containers | 1 × 40' HQ (per current workbook input) |
| Main freight | $8,350.00 |
| Transit time | 33 days, departure to arrival (historical quote input) |
| Arrival to sellable stock | 14 days (workbook planning input; not confirmed by the 3PL rate sheet) |
| Destination port / terminal / drayage | $140.00 |
| Customs brokerage, ISF, bond | $15.00 |
| Cargo insurance | $16.91 |
| Destination charges subtotal | $171.91 |
| Origin charges | $0.00 in the workbook because the selected Incoterm is FOB; verify quote scope before treating every origin component as included |
| Workbook duty & tariff estimate | $16,668.96 — calculated from Shipment Setup, **not a Flexport-confirmed duty quote** |

**Important:** Retain these values as historical quote inputs only. Request a refreshed freight quote and reconfirm route, container type, included charges, destination delivery, transit estimate, and validity before using them for a booking or current provider comparison.

### B. General 2026 Flexport 3PL rate sheet

Jordan's email response dated November 19, 2026 stated that Flexport can provide B2B, B2C, and transload services through a network of more than 9 million square feet across its own and partner warehouses. Jordan identified container-receiving capability at Los Angeles, Long Beach, and Oakland, with additional own/partner facilities across the US and Canada.

| Service | Flexport rate / response | Scope and caveat |
|---|---:|---|
| Palletized container receiving / unloading — 20' | $345/container | General rate sheet |
| Palletized container receiving / unloading — 40' / 40' HQ / 45' HQ | $490/container | General rate sheet; current workbook uses $490 for one 40' HQ |
| Non-palletized unloading | $0.30/carton | Alternative to palletized container receiving; do not add both for the same unload |
| Palletizing, wrap included | $16.50/pallet | General rate sheet |
| Storage | $2.75/pallet/day | Four free days included; chargeable storage begins after free days |
| Inventory handling | $45/man-hour | When applicable |
| FBA labeling | $0.35/label | General rate sheet |
| Rework / VAS | Per work required | No fixed rate supplied; obtain task-specific pricing |
| Photos | No extra charge | Per email |
| Strapping | $35/strap | General rate sheet |
| LTL forwarding to Amazon | Location-specific | No rate supplied; Jordan requested destination addresses to price |
| Warehouse coverage | LA, Long Beach, Oakland named for container receiving | Confirm exact facility, service availability, and routing for the actual shipment |

**Commercial caveats from the email:** Rates are subject to Flexport terms, availability, tariffs, surcharges, and regulatory changes. The email states that the rate sheet is not a binding agreement unless confirmed in writing. Obtain a shipment-specific written quote before relying on any rate.

**Storage normalization:** For a seven-day stay, the rate-card equivalent is three chargeable days after the four free days:
- $2.75 × (7 − 4) = **$8.25 per pallet** for that seven-day stay.
- At 38 pallets: 38 × $8.25 = **$313.50**.
- This is not a general weekly rate for longer stays. Use the daily formula: pallets × max(0, storage days − 4) × $2.75, subject to Flexport confirming how free days apply to the actual receiving/storage arrangement.

## 2. Current workbook scenario — Scenario 2

The current workbook scenario supplied on November 20 models one FCL container and 5,808 Classic Food Mill units routed to AWD through a 3PL hub.

### Freight and shipment inputs

| Input | Workbook value | Evidence classification |
|---|---:|---|
| Units allocated to AWD | 5,808 | Shipment Setup / workbook input |
| Units to FBA direct, Walmart WFS, TikTok FBT | 0 | Workbook allocation |
| Containers | 1 | Workbook input |
| Main freight | $8,350.00 | Historical Flexport quote; expired |
| Destination charges | $171.91 | Historical quote inputs; expired |
| Transit days | 33 | Historical quote input |
| Days from arrival to sellable stock | 14 | Planning input; validate |
| Pallets received | 38 | Workbook calculation / shipment assumption |
| Cartons | 834 | Shipment scenario assumption used in prior model notes |
| CBM per pallet | 1.80 | Workbook assumption |

### Hub and last-mile inputs

| Workbook field | Current value | Classification |
|---|---:|---|
| Container unload per container | $490.00 | Flexport rate-card value for palletized 40' HQ receiving |
| Receive / palletize per pallet | $16.50 | Flexport rate-card value; describe as palletizing (wrap included) |
| Sort / re-carton per carton | $0.40 | Internal model assumption; not quoted by Flexport |
| Channel labels per carton | $0.30 | Internal model assumption; not the same as Flexport's $0.30 non-palletized unloading rate |
| Outbound pallet build per pallet | $14.00 | Internal model assumption; not quoted by Flexport |
| Handling + admin per outbound delivery | $100.00 | Internal model assumption; not quoted by Flexport |
| Storage per pallet for a seven-day stay | $8.25 | Derived from Flexport's $2.75/day rate and four free days |
| Days before split | 7 | Planning assumption |
| LTL to AWD / FBA per pallet | $160.00 | Workbook rate-card assumption; **not Flexport-quoted** |
| LTL to Walmart WFS per pallet | $190.00 | Workbook rate-card assumption; **not Flexport-quoted** |
| LTL to TikTok FBT per pallet | $180.00 | Workbook rate-card assumption; **not Flexport-quoted** |
| Full-truckload cap per destination | $2,400.00 | Workbook rate-card assumption; **not Flexport-quoted** |
| LTL minimum per delivery | $175.00 | Workbook rate-card assumption; **not Flexport-quoted** |
| Appointment / liftgate per delivery | $25.00 | Workbook rate-card assumption; **not Flexport-quoted** |

### Current workbook outputs (as supplied)

| Output | Workbook result |
|---|---:|
| Main freight | $8,350.00 |
| Destination port, brokerage, insurance | $171.91 |
| Duty & tariff | $16,668.96 |
| Delivery to AWD, including hub last mile | $2,425.00 |
| Hub storage, handling & AWD fees | $7,408.97 |
| Total landed cost | $35,024.84 |
| Cost per unit | $6.03 |
| Transit + time to sellable stock | 47 days |
| Hub fees total (Section 8) | $2,826.99 |
| Last mile to AWD (Section 9) | $2,425.00 |
| AWD fees (Section 10) | $4,091.98 |
| Cost of splitting load: hub + last mile | $5,251.99 |

These are copied workbook outputs, not a Flexport quote or independently certified model results. The duty estimate and Amazon AWD fees are separate model inputs/calculations, not Flexport charges.

## 3. Reconciliation items before relying on the scenario

1. **Expired freight quote:** Refresh Quote-5822787 before using the $8,350 freight and $171.91 destination charges as current pricing.
2. **Unquoted hub services:** Sort/re-carton, channel labeling, outbound pallet build, and handling/admin remain internal assumptions. Do not describe them as Flexport rates.
3. **Outbound delivery:** Flexport has not supplied the LTL rate to the actual AWD facility. The workbook's $160/pallet and related last-mile values are generic assumptions, not provider-confirmed.
4. **Potential $490 receiving double count:** Section 6 currently has a $490 3PL/hub storage and handling entry, while Section 8 separately includes $490 container unloading. Section 8's calculated hub fees may already include the container unload. Inspect the workbook formulas and confirm whether the same receiving charge is included twice before relying on the total.
5. **Hub-fee calculation:** The supplied Section 8 hub-fee output is $2,826.99. Reconcile it against the individual inputs and formula logic; do not assume it is correct solely because the workbook calculates it.
6. **Combined outputs:** The $7,408.97 hub storage/handling/AWD output and $35,024.84 total landed cost inherit any duplicate charges or unverified assumptions above. Treat them as provisional.
7. **Duty/tariff:** The $16,668.96 amount is a Shipment Setup calculation. Validate the product customs value, classification, and applicable rates with the appropriate customs source/broker.
8. **Amazon AWD fees:** The $4,091.98 AWD processing/storage amount is an Amazon-side model calculation, not a Flexport fee. Verify the rate card and assumptions independently.
9. **Inbound placement fee:** The workbook's $0.63 default is not a Flexport charge. The current scenario allocates all 5,808 units to AWD and zero to FBA direct, so the output shows $0 inbound placement fees.

## 4. Follow-up needed from Flexport

Once the standard 3PL rate comparison has been gathered and the project is ready for targeted follow-up, request:

- A refreshed freight quote for the actual origin, 40' HQ shipment, and final destination.
- Confirmation of which LA / Long Beach facility can receive the container and whether the $490 palletized receiving rate applies to this shipment.
- A written quote for LTL delivery to the exact AWD destination address, including appointment, liftgate, fuel, accessorial, and minimum charges.
- Confirmation of storage free-time calculation and any minimum storage billing.
- Task-specific pricing for sorting/re-cartoning, channel labeling, outbound pallet preparation, and any required FBA prep/VAS.
- Confirmation of any additional account, receiving, transload, or handling charges not shown on the general rate sheet.

**Current project sequencing:** The immediate management priority is to collect standard 3PL rate sheets and compare them. Keep detailed Flexport follow-up questions as quote gaps to address after the standard rate-sheet collection, rather than expanding the initial outreach.

## 5. Related records

- [R6 — Logistics Optimization](./R6-logistics-optimization.md)
- [R6 — Progress Update Log](./R6-update-log.md)
- [Shipment Logistics Comparison Workbook Audit](./shipment-comparison-workbook-audit.md)
- [Go-to RFQ Playbook](./go-to-rfq.md)
- [HA Shipment Logistics Comparison workbook](https://docs.google.com/spreadsheets/d/1kHKgk26CfQT1QtTZmA09Qf7l5dMD5mijonewIB6E1Ug/edit?gid=100#gid=100)
