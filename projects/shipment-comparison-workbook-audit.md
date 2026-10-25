# Shipment Logistics Comparison Audit

This document explains how to use the **Shipment Logistics Comparison** workbook. It includes a tab-by-tab operational guide, a checklist of data to request from freight forwarders and 3PLs, and a step-by-step scenario analysis workflow.

## 1. Workbook Audit & Architecture Overview

### Purpose

The workbook evaluates and compares **Total Landed Cost** and **Cost per Unit** across four logistics routing paths for a single shipment load:

1. **Amazon Path (AGL):** China origin → Amazon Global Logistics (AGL) → Amazon Warehousing & Distribution (AWD) → FBA Direct, Walmart WFS, or TikTok FBT.
2. **Scenario 1:** Third-party freight forwarder / 3PL quote option A.
3. **Scenario 2:** Third-party freight forwarder / 3PL quote option B.
4. **Scenario 3:** Third-party freight forwarder / 3PL quote option C.

### Data Flow Architecture

```text
[Products (Master)] + [Rate Card (Amazon Reference Fees)]
                            |
                            v
                    [Shipment Setup]
        (SKUs, quantities, channels, cost allocation method)
                            |
          +-----------------+-----------------+
          |                 |                 |
          v                 v                 v
 [Amazon Path (AGL)] [Scenarios 1, 2, 3] [Customs & Duty]
     (AGL quote)     (Forwarder / 3PL)    (Auto-calculated)
          |                 |                 |
          +-----------------+-----------------+
                            |
                            v
                      [Comparison]
             (Landed cost, delta %, time, cost/unit)
                            |
                            v
                 [Checks & Shipment Log]
             (Validation audit and historical archive)
```

## 2. Tab-by-Tab Usage & Cell Reference Guide

### 2.1 Color Coding System

- **Yellow background / blue text:** Manual input cells. Enter data here.
- **Cream background:** Calculated or formula cells. Do not overwrite.
- **Grey background:** Non-applicable cells based on the selected Incoterm or transit mode.

### 2.2 Master Reference Tabs

Maintain these tabs regularly.

#### 1. `Products` — Product Master

**Purpose:** Stores SKU physical specifications, unit costs, and HTS duty schedules.

**Key inputs (columns A–P):**

- `Product` and `SKU / ASIN`: Product names and identifiers.
- `Units per carton`, `Carton L/W/H (cm)`, `Carton gross kg`: Physical specifications used to calculate CBM and chargeable weight.
- `Unit COGS ($)`: Product cost basis used in duty calculations.
- `HTS code`, `Base duty %`, `Tariff % (Section 301)`: Applicable tariff and duty inputs.
- `AWD inbound + processing $/unit`, `AWD to FBA transfer $/unit`: Channel handling rates.

**Calculated field:**

- `CBM per carton` = \(L \times W \times H \div 1{,}000{,}000\), where dimensions are in centimeters.

#### 2. `Rate Card` — Reference Rates

**Purpose:** Standardizes Amazon baseline fees for comparison.

**Key inputs:**

- `Inbound placement fee ($/unit)`: FBA Direct inbound placement fee.
- `AWD storage ($/CBM/month)`: Reference AWD storage rate.
- `Air volumetric factor`: Default of 167 kg/CBM.
- `Date verified`: Tracks rate freshness. Review and verify at least every 60 days.

### 2.3 Active Shipment Tabs

These tabs contain the inputs and calculations for each shipment load.

#### 3. `Shipment Setup` — Primary Inputs

**Purpose:** Defines shipment details, order quantities, and multichannel allocation.

**Key inputs:**

- **Shipment metadata:** `Shipment name / PO`, `Date`, `Origin port / factory`.
- **Cost settings:**
  - `Allocate shared costs by`: `CBM` or `Weight`.
  - `Include cost of capital?`: `Yes` or `No`.
  - `Annual cost of capital %`.
- **Product matrix (rows 13+):** Select products, enter order quantities, and allocate units to:
  - `To AWD (units)`
  - `To FBA direct (units)`
  - `To Walmart WFS (units)`
  - `To TikTok FBT (units)`

**Validation:** Confirm that `Unallocated units` equals **0** for every applicable product row.

#### 4. `Amazon Path (AGL)`

**Purpose:** Models costs for shipping through Amazon Global Logistics and AWD.

**Key inputs:**

- `AGL quote reference` and `Quote valid until`.
- `Mode`: `FCL`, `LCL`, or `Air`.
- `Transit days (departure to AWD receipt)` and `Days from AWD to sellable`.
- Freight inputs, according to mode:
  - `FCL price/container`
  - `LCL rate/CBM`
  - `Air rate/kg`
- `Customs brokerage, ISF, bond ($)`.
- `Cargo insurance ($)`.
- `Average months stored in AWD`.
- Channel transfer fees, including `AWD to Walmart WFS` and `AWD to TikTok FBT`.

#### 5–7. `Scenario 1`, `Scenario 2`, and `Scenario 3`

**Purpose:** Model independent freight forwarder and 3PL routing alternatives.

**Key inputs:**

- **Quote details:** Forwarder name, quote reference, validity date, `Incoterm` (`EXW`, `FOB`, or `DDP`), and `Mode` (`FCL`, `LCL`, or `Air`).
- **Freight rates:** Enter the rate matching the selected mode and Incoterm, such as `DDP all-in`, `FCL price/container`, `LCL rate/CBM`, or `Air rate/kg`.
- **Origin charges (Section 3 — EXW only):** Factory pickup, export clearance, and origin handling / THC.
- **Destination charges (Section 4 — EXW and FOB):** Destination port / terminal charges, customs brokerage, and cargo insurance.
- **Delivery to destinations (Section 5):** Separate delivery rates to AWD, FBA Direct, Walmart WFS, and TikTok FBT.
- **Fees and storage (Section 6):** Inbound placement fees per unit and 3PL hub storage / handling fees.

> **Important:** Confirm which services are included in each quote to avoid double-counting or omitting charges. Treat DDP quotes according to their documented scope and exclusions.

### 2.4 Output & Audit Tabs

#### 8. `Comparison` — Decision Matrix

**Purpose:** Aggregates and compares all four routing paths side by side.

**Outputs:**

- **Landed cost breakdown:** Freight, origin, destination, duty / tariffs, delivery, placement fees, and hub storage.
- **Total landed cost** and **cost per unit**.
- **Cost delta vs. AGL:** Dollar and percentage savings or premium relative to the Amazon path.
- **Cost-of-capital-adjusted cost:** Accounts for inventory holding costs associated with transit time.
- **Decision flags:** Identifies the cheapest and fastest options.
- **Segmented unit costs:** Cost per unit by destination channel and product SKU.

#### 9. `Checks` — Quality Audit

**Purpose:** Validates inputs before a routing decision is made.

**Audit rules:**

- Confirms that product master data, including CBM, weight, and unit COGS, is populated.
- Verifies that unallocated units equal 0 in `Shipment Setup`.
- Checks whether quote validity dates have expired.
- Flags Rate Card information that has not been verified within the last 60 days.

#### 10. `Shipment Log` — Historical Archive

**Purpose:** Maintains a historical record of shipment costs and routing decisions.

**Workflow:**

1. Copy the values from `Comparison` cells `B28:E28`.
2. Paste the values into the `Shipment Log`.
3. Record the PO number, selected routing path, realized or estimated savings as appropriate, and relevant notes.

## 3. Data Required from Freight Forwarders & 3PLs

To populate `Scenario 1`, `Scenario 2`, and `Scenario 3`, request an itemized quote covering the relevant line items below.

| Category | Required line item / metric | Applies to | Notes |
|---|---|---|---|
| **Quote header** | Quote reference, expiration date, Incoterm (`EXW`, `FOB`, `DDP`), and mode (`FCL`, `LCL`, `Air`) | All | Ensures quote validity and correct workbook inputs. |
| **Transit time** | Port-to-port transit days and inland delivery lead time to the warehouse | All | Used to estimate time to sellable inventory and cost of capital. |
| **Origin charges** | Factory pickup / trucking, export customs clearance, origin THC / handling | EXW only | Confirm which charges are already included under other Incoterms. |
| **Main freight** | FCL rate per container, LCL rate per CBM and minimum charge, or air rate per kg | EXW, FOB | For air freight, verify the applicable volumetric factor; workbook default is 167 kg/CBM. |
| **Destination fees** | Destination terminal handling (DTHC), drayage, deconsolidation | EXW, FOB | Identify destination port-to-hub charges. |
| **Customs and bond** | Customs brokerage, ISF filing, single-entry or annual bond | EXW, FOB | Confirm the responsible party and whether each fee is included. |
| **Cargo insurance** | Total cargo insurance premium | EXW, FOB | Confirm the insured value and calculation basis. |
| **Last-mile trucking** | Separate delivery charges to AWD, FBA Direct, Walmart WFS, and TikTok FBT | EXW, FOB | Request costs for each applicable destination. |
| **3PL hub fees** | Receiving / palletization, monthly storage, outbound preparation / transfer | 3PL routing | Required when using a private 3PL hub instead of direct routing to AWD. |
| **All-in price** | Door-to-door rate per shipment or per unit | DDP only | Confirm whether duties, tariffs, clearance, and final delivery are included. Document exclusions. |

### External Information → Workbook Input Mapping

Use this table internally to translate a provider’s natural response and quote into workbook inputs. It is **not** a checklist to send wholesale to every forwarder. “Required” means required to make a defensible comparison; if a value is unavailable, record it as unknown and follow up when material instead of guessing.

| Workbook field / cost category | Who should supply it | Required to compare? | Targeted follow-up if missing | How to record unknown / unconfirmed data |
|---|---|---|---|---|
| Provider, quote reference, quote date, validity | Forwarder | Yes | “Could you confirm the quote reference and how long the price is valid?” | Mark pending; do not treat an expired or undated rate as confirmed. |
| Incoterm, pricing basis, included / excluded services | Forwarder | Yes | “What is included in this price, and which charges would be billed separately?” | Mark scope **unclear**; do not compare headline totals as equivalent. |
| Delivered price and named destination | Forwarder | Yes for delivered comparison | “Does this price include final delivery to [facility/address]?” | Record destination or delivery scope as pending; exclude from a like-for-like conclusion until clarified. |
| Logistics-only freight and service charges | Forwarder | Strongly preferred; required to normalize an itemized scenario | “Could you share the logistics-only breakdown, if available?” | Enter only documented charges; mark missing line items unknown rather than zero. |
| Route, mode, container configuration | Forwarder | Yes | “What route and container/mode have you priced?” | Record as provider estimate / pending validation; do not assume a port or container. |
| Origin pickup, export clearance, origin handling | Forwarder; supplier confirms pickup facts | Required when applicable and not included elsewhere | “Are pickup, export clearance, and origin handling included or separate?” | Mark included / excluded / separately quoted / unclear; avoid double-counting. |
| Main freight rate and minimums | Forwarder | Yes | “What is the rate basis and are there minimum charges?” | Preserve quoted unit and currency; do not convert without a documented basis. |
| Destination terminal, drayage, deconsolidation, handling | Forwarder | Required unless explicitly included or not applicable | “Are there destination or handling charges beyond the quoted price?” | Mark unknown or included only with written support; do not enter $0 just because omitted. |
| Customs brokerage, filings, bond, duties, tariffs, taxes | Forwarder and/or customs broker, depending on scope | Required to establish landed-cost scope; exact tax/duty values may need specialist confirmation | “Who handles entry, and are brokerage, duties, tariffs, taxes, and bond included or separate?” | Separate provider quote from broker-confirmed duty/tax assumptions; flag unresolved compliance costs. |
| Cargo insurance | Forwarder / insurer; internal cargo value from current commercial invoice | Required if included in the comparison assumptions; otherwise explicitly disclose exclusion | “Is cargo insurance included? If not, can you quote it separately?” | Mark excluded, separately quoted, or unknown; do not infer coverage. |
| Final-mile delivery to AWD / FBA Direct / WFS / FBT | Forwarder or delivery provider | Required for each destination being modeled, unless included in delivered price | “Does the quote cover delivery to [exact destination], including appointment requirements?” | Populate only applicable destinations; missing rates remain unknown, not zero. |
| Transit / door-to-door lead time and departure frequency | Forwarder | Yes for time/risk comparison | “What is the estimated door-to-door lead time, and how often does this route depart?” | Label estimates as estimates; distinguish port-to-port from total lead time. |
| Payment terms, free time, demurrage/detention, surcharges | Forwarder | Material commercial terms required before booking; include in cost comparison when applicable | Ask only about the term that is missing or could materially affect cost. | Record as pending / subject to confirmation; do not invent an allowance. |
| Cartons, units, dimensions, gross weight, CBM, cargo value | Supplier documents; internal shipment records | Yes for reliable pricing and cost allocation | Ask supplier for the missing packing-list or invoice detail; then share relevant verified figures with the forwarder. | Mark supplier confirmation pending; never estimate physical specifications or cargo value. |
| Product COGS, SKU mix, HTS classification, duty assumptions | Internal product records and qualified customs specialist | Required for applicable workbook duty / landed-cost calculations; not normally a forwarder’s basic quote input | Verify product master; ask broker/specialist to confirm classification and applicable rates. | Keep assumptions visibly flagged; do not present unverified tariff values as confirmed. |
| Amazon placement fees, AWD storage/processing, channel transfer costs | Internal Rate Card / current Amazon references | Required when relevant to the route being modeled, not a forwarder input | Verify the relevant rate and date internally. | Mark stale or unverified reference rates; follow the workbook’s rate-freshness checks. |
| Shipment allocation, shared-cost method, cost of capital | Internal shipment plan and approved analysis assumptions | Required for the chosen comparison model, not a forwarder input | Confirm internally with the responsible owner if unclear. | Label assumptions and run sensitivity analysis if a material input is uncertain. |

**Recording rule:** Use the workbook’s available fields and notes to distinguish **confirmed**, **provider estimate**, **internal assumption**, **included**, **excluded**, **separately quoted**, **unknown**, and **pending confirmation**. A missing charge is not zero. Do not make a final like-for-like recommendation while a material cost or service-scope gap remains unresolved.

**RFQ principle:** Ask for a clear delivered price and, where practical, a logistics-only breakdown. The provider can answer naturally; we own the work of mapping, checking, and normalizing the quote internally.

## 4. Step-by-Step Scenario Analysis Workflow

### Step 1: Prepare Master Data

1. Open `Products`.
2. Verify that carton dimensions (\(L \times W \times H\)), carton weights, unit COGS, HTS codes, and applicable duty / tariff percentages are populated for every SKU in the planned order.
3. Open `Rate Card`.
4. Confirm Amazon placement fees and AWD storage rates have been verified within the last 60 days.

### Step 2: Define Shipment Parameters

1. Open `Shipment Setup`.
2. Enter the PO / shipment name, date, and origin port or factory.
3. Select the product SKUs and enter total order quantities.
4. Allocate units across:
   - `To AWD`
   - `To FBA direct`
   - `To Walmart WFS`
   - `To TikTok FBT`
5. Verify that `Unallocated units` equals **0** for all applicable rows.
6. Choose the shared-cost allocation basis: `CBM` or `Weight`.
7. Choose whether to include cost of capital and enter the annual rate if applicable.

### Step 3: Populate the Amazon Path (AGL)

1. Open `Amazon Path (AGL)`.
2. Enter the AGL quote reference, expiration date, mode, and applicable freight rate.
3. Enter estimated transit days and the time from AWD receipt to sellable inventory.
4. Enter applicable brokerage, insurance, storage, and channel transfer costs.

### Step 4: Populate Forwarder Scenarios

1. Open `Scenario 1`, then `Scenario 2` and `Scenario 3` if comparing additional providers.
2. Enter the forwarder name, quote reference, validity date, Incoterm, and mode.
3. Populate the applicable freight costs.
4. Enter origin charges for EXW quotes and destination charges for EXW / FOB quotes, as applicable.
5. Enter delivery costs for each relevant destination channel.
6. Record any 3PL storage, handling, or transfer fees.
7. Confirm all included services, exclusions, and quote assumptions before comparing totals.

### Step 5: Run the Operational Audit

1. Open `Checks`.
2. Confirm all applicable checks display **OK**.
3. If any check displays **CHECK**, **EXPIRED**, or **VERIFY**, return to the indicated tab and resolve the issue before making a business decision.

### Step 6: Evaluate Comparative Results

1. Open `Comparison`.
2. **Cost comparison:** Review row 27 (`TOTAL LANDED COST`) and row 28 (`Cost per unit`).
3. **Savings analysis:** Review rows 29 and 30 (`Difference vs Amazon path $ / %`) to quantify the cost difference relative to AGL.
4. **Time-versus-cost trade-off:** Review the **Fastest** and **Cheapest** flags. If a third-party forwarder is cheaper but takes longer, assess whether the savings outweigh additional inventory holding costs and stockout risk.
5. **Channel costing:** Review `COST PER UNIT BY DESTINATION` to identify whether specific channels, such as FBA Direct, are more economical under particular routing options.
6. Verify that differences between options reflect equivalent service scopes and all applicable fees.

### Step 7: Log the Decision

1. Once a routing path is selected, copy the final comparison values from `Comparison` cells `B28:E28`.
2. Paste values into the `Shipment Log`.
3. Record the PO / shipment name, selected path, estimated or realized savings, and relevant decision notes.
4. Preserve the supporting quotes and assumptions so the decision can be reviewed later.

---

## 5. Audit Limitations & Decision Guardrails

- **Quote comparability:** Different Incoterms and service scopes can make headline rates misleading. Normalize included services and exclusions before comparing totals.
- **Amazon ecosystem benefits:** Consider applicable inbound placement fee waivers, AGL pricing advantages, and AWD-related benefits when assessing the total cost of changing routes.
- **Cost of capital:** Treat results as estimates based on the assumptions entered in the workbook, not guaranteed realized savings.
- **Data freshness:** Reverify rates and fees when they expire or when material changes are announced.
- **Customs and compliance:** Confirm HTS classification, applicable duty / tariff rates, and import requirements with the appropriate customs broker or specialist.
- **Decision quality:** The cheapest option is not automatically the best option. Consider delivery timing, reliability, service coverage, inventory risk, and the operational consequences of changing routes.

**Core principle:** Use the workbook to support a documented, evidence-based logistics decision. Validate the inputs before relying on the outputs, and preserve the quotes and assumptions behind the final recommendation.

## 6. Review of the Actual Workbook (October 2026)

This section records findings from inspecting the uploaded `HA Shipment Logistics Comparison (DRAFT).xlsx` workbook, including its formulas, input coverage, and current readiness. It supplements the usage guide above; it does not certify the model as fully validated.

### Current Readiness

**Assessment: useful comparison framework, but not yet ready to support a real routing decision without verified inputs and a shipment-level validation.**

The workbook has a clear input-to-output structure across `Shipment Setup`, `Products`, `Rate Card`, the AGL and scenario tabs, `Comparison`, `Checks`, and `Shipment Log`. Its formulas attempt to allocate shared costs, calculate landed cost and cost per unit, and compare route totals. However, a formula returning a number is not proof that the input is complete or that the model matches the provider's actual service scope.

### Findings to Resolve Before Using Real Shipment Results

1. **Replace or clear example-like shipment inputs.** The inspected `Shipment Setup` contained 1,000 Classic Food Mill units, allocated as 500 to AWD, 250 to FBA Direct, 100 to Walmart WFS, and 150 to TikTok FBT. Treat these as seed/example values—not approved quantities, a booking instruction, or verified shipment allocation. Enter the actual shipment plan before analysis.
2. **Complete and verify product master data.** Carton dimensions/CBM, gross carton weight, unit COGS, HTS classification, and applicable duty/tariff assumptions were incomplete or unverified. These inputs affect pricing, cost allocation, and landed-cost calculations. Obtain physical specifications from supplier packing documents and validate customs assumptions with the appropriate broker or specialist.
3. **Verify current reference rates.** Rate Card values and verification dates need review against current authoritative Amazon references. The workbook's freshness check is a prompt to verify, not evidence that a rate is correct.
4. **Do not interpret missing-input zeros as zero cost.** Some calculations can display zero when source inputs are blank. A zero output is not reliable evidence that the charge does not apply. Resolve the input or explicitly mark the charge unknown / excluded and disclose the limitation.
5. **Validate DDP scope to prevent double-counting or omission.** Confirm in writing which services a DDP quote includes—such as origin charges, main freight, customs clearance, duties/tariffs, destination charges, and final delivery. The scenario model may add other costs to a DDP price; this is only appropriate where those costs are explicitly outside the quote. Do not assume every DDP quote has the same inclusions.
6. **Treat cost allocation and comparison outputs as model estimates.** The workbook allocates shared costs and calculates product/channel costs, but those outputs still depend on complete inputs, correct assumptions, and equivalent service scopes. Run the `Checks` tab, inspect material inputs, and reconcile the calculated totals before relying on the cheapest/fastest flags.
7. **Do not fill every scenario merely because three are available.** Start with one actual shipment and two genuinely comparable paths—typically AGL versus one alternative with a sufficiently clear quote. Add other scenarios only when there is a real provider quote worth evaluating. This keeps the analysis focused on the current bottleneck: obtaining comparable, verified quotes.

### Recommended Validation Sequence

1. Choose one real shipment and confirm its SKU mix, quantities, carton counts, dimensions, gross weight, cargo value, and destination allocation from authoritative records.
2. Verify the current AGL quote or shipment cost breakdown, including its route, quote/booking reference, validity, service scope, and applicable AWD/channel costs.
3. Enter one alternative provider quote only after its Incoterm, route, delivery destination, inclusions, exclusions, and material additional charges are clear.
4. Keep unknown amounts marked as unknown; do not enter zero as a placeholder for an unconfirmed charge.
5. Run `Checks`, inspect the relevant formula outputs, reconcile cost totals, and confirm both paths represent comparable service scope.
6. Record assumptions, unresolved gaps, and source documents with the result. Do not make a recommendation while a material cost, destination, customs, or service-scope gap remains open.

### Current Working Example: FCLGO RFQ

The current FCLGO request covers **two 40' HQ containers** from China to Amazon AWD in Southern California, with **11,808 total units** across Classic and Compact Food Mills:

- Classic Food Mill: 5,808 units × $7.48 = $43,443.84 product value.
- Compact Food Mill: 6,000 units × $7.12 = $42,720.00 product value.
- Total product value: $86,163.84.

These figures describe the current RFQ scope, not a confirmed freight quote or final landed cost. FCLGO acknowledged the request on October 24 but had not yet supplied the requested itemized quotation. The quoted scope still needs confirmation for ocean freight, origin and destination charges, customs/clearance, duties, AWD final-mile delivery, and transit time. Supplier/broker confirmation is also pending for any required import documentation; do not state that a specific document or filing is available until confirmed.

Before using this shipment in the workbook, obtain verified carton dimensions and gross weights, confirm the exact AWD delivery facility/address, and source the AGL comparison from a current booking/quote or reliable shipment cost record. Preserve the quote and any assumptions used.

### Known Limitation

This is an input-readiness and workflow audit, not a full formula certification. The formulas were reviewed at a high level, but every calculation has not been independently validated against a completed real shipment. Confirm the model against actual quote scopes and known shipment costs before treating its outputs as decision-grade.

