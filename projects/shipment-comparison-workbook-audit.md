<!-- HA Operations shared navigation -->
[HA Operations](../README.md) · [R6 Rock](./R6-logistics-optimization.md) · [R6 Progress Log](./R6-update-log.md) · [Shipment Comparison Audit](./shipment-comparison-workbook-audit.md)

---
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

**RFQ principle:** Ask forwarders to itemize charges even when they offer an all-in price. This makes it easier to compare quotes on an equivalent service basis.

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
