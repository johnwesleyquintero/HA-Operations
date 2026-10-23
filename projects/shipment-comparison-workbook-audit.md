# Shipment Logistics Comparison Audit

This audit provides a guide on how to use the **Shipment Logistics Comparison** workbook, including a tab-by-tab operational breakdown, a checklist of data to request from Freight Forwarders and 3PLs, and a step-by-step scenario analysis workflow.-----### 1\. Workbook Audit & Architecture Overview#### PurposeThe workbook is designed to evaluate and compare the **Total Landed Cost** and **Cost per Unit** across **four distinct logistics routing paths** for a single shipment load:1.  **Amazon Path (AGL):** China origin $\\rightarrow$ Amazon Global Logistics (AGL) $\\rightarrow$ Amazon Warehousing & Distribution (AWD) $\\rightarrow$ FBA Direct / Walmart WFS / TikTok FBT.
2.  **Scenario 1:** Third-Party Freight Forwarder / 3PL Quote Option A.
3.  **Scenario 2:** Third-Party Freight Forwarder / 3PL Quote Option B.
4.  **Scenario 3:** Third-Party Freight Forwarder / 3PL Quote Option C.

#### Data Flow Architecture

``` 
  [Products (Master)]   +   [Rate Card (Amazon Reference Fees)]
                                  │
                                  ▼
                        [Shipment Setup] 
         (SKUs, Quantities, Channels, Cost Allocation Method)
                                  │
         ┌────────────────────────┼────────────────────────┐
         ▼                        ▼                        ▼
[Amazon Path (AGL)]     [Scenario 1, 2, 3]         [Customs & Duty]
   (AGL Quote)        (3PL / Forwarder Quotes)    (Auto-calculated)
         │                        │                        │
         └────────────────────────┼────────────────────────┘
                                  ▼
                            [Comparison]
              (Landed Cost, Delta %, Time, Cost/Unit)
                                  │
                                  ▼
                       [Checks & Shipment Log]
               (Validation Audit & Historical Archive)

```

-----

### 2\. Tab-by-Tab Usage & Cell Reference Guide#### A. Color Coding System  * **Yellow Background / Blue Text:** Manual Input Cells (Enter data here).
  * **Cream Background:** Calculated / Formula Cells (Do NOT overwrite).
  * **Grey Background:** Non-applicable cells based on chosen Incoterm or transit mode.

-----

#### B. Master Reference Tabs (Maintain Regularly)1.  **`Products` (Product Master)**
    
      * **Purpose:** Stores SKU physical specs, unit costs, and HTS duty schedules.
      * **Key Inputs (Columns A–P):**
          * `Product` & `SKU / ASIN`: Item names and identifiers.
          * `Units per carton`, `Carton L/W/H (cm)`, `Carton gross kg`: Physical dimensions used to compute CBM and chargeable weight.
          * `Unit COGS ($)`: Customs valuation basis for duty calculations.
          * `HTS code`, `Base duty %`, `Tariff % (Section 301)`: Tariff rate percentages.
          * `AWD inbound + processing $/unit`, `AWD to FBA transfer $/unit`: Channel handling rates.
      * **Calculated Fields:** `CBM per carton` ($L \\times W \\times H / 1,000,000$).

2.  **`Rate Card` (Reference Rates)**
    
      * **Purpose:** Standardizes Amazon baseline fees for comparison.
      * **Key Inputs:**
          * `Inbound placement fee ($/unit)` for FBA direct shipments.
          * `AWD storage ($/CBM/month)`.
          * `Air volumetric factor` (Default: $167\\text{ kg/CBM}$).
          * `Date verified`: Keeps track of fee freshness (should be updated every 60 days).-----#### C. Active Shipment Tabs (Per Shipment Load)3.  **`Shipment Setup` (Primary Inputs)**
    
      * **Purpose:** Defines the shipment details, order quantities, and multichannel allocation.
      * **Key Inputs:**
          * **Shipment Meta:** `Shipment name / PO`, `Date`, `Origin port / factory`.
          * **Cost Settings:** `Allocate shared costs by` (`CBM` or `Weight`), `Include cost of capital?` (`Yes` / `No`), `Annual cost of capital %`.
          * **Product Matrix (Rows 13+):** Select products, enter `Units` ordered, and assign unit destinations:
              * `To AWD (units)`
              * `To FBA direct (units)`
              * `To Walmart WFS (units)`
              * `To TikTok FBT (units)`
      * **Validation Cell:** Ensure `Unallocated units` column is **0** across all rows.

4.  **`Amazon Path (AGL)`**
    
      * **Purpose:** Costing model for shipping via Amazon Global Logistics & AWD.
      * **Key Inputs:**
          * `AGL quote reference`, `Quote valid until`, `Mode` (`FCL`, `LCL`, or `Air`).
          * `Transit days (departure to AWD receipt)` & `Days from AWD to sellable`.
          * Freight rate inputs (`FCL price/container`, `LCL rate/CBM`, or `Air rate/kg`).
          * `Customs brokerage, ISF, bond ($)` and `Cargo insurance ($)`.
          * `Average months stored in AWD`.
          * Channel transfer fees (`AWD to Walmart WFS`, `AWD to TikTok FBT`).

5.  **`Scenario 1`, `Scenario 2`, `Scenario 3` (3PL / Freight Forwarder Quotes)**
    
      * **Purpose:** Costing models for independent freight forwarders and 3PL routing.
      * **Key Inputs:**
          * **Quote Details:** Forwarder Name, Quote Ref, Valid Until, `Incoterm` (`EXW`, `FOB`, or `DDP`), `Mode` (`FCL`, `LCL`, `Air`).
          * **Freight Rate Inputs (Section 2):** Input rates matching the chosen mode (`DDP all-in`, `FCL price/container`, `LCL rate/CBM`, or `Air rate/kg`).
          * **Origin Charges (Section 3 - EXW only):** Factory pickup, export clearance, origin handling/THC.
          * **Destination Charges (Section 4 - EXW & FOB):** Destination port/terminal charges, customs brokerage, cargo insurance.
          * **Delivery to Destinations (Section 5):** Direct trucking rates to `AWD`, `FBA direct`, `Walmart WFS`, and `TikTok FBT`.
          * **Fees & Storage (Section 6):** Inbound placement fee $/unit and 3PL hub storage/handling fees.-----#### D. Output & Audit Tabs6.  **`Comparison` (Decision Matrix)**
    
      * **Purpose:** Aggregates and compares all four paths side-by-side.
      * **Outputs Provided:**
          * **Landed Cost Breakdown:** Freight, Origin, Destination, Duty/Tariffs, Delivery, Placement Fees, Hub Storage.
          * **Total Landed Cost** & **Cost per Unit**.
          * **Cost Delta vs AGL:** Dollar ($) and percentage (%) savings or premium compared to Amazon.
          * **Cost of Capital Adjusted Cost:** Factors in holding cost during transit time.
          * **Decision Flags:** Highlights **Cheapest** and **Fastest** options.
          * **Segmented Unit Costs:** Cost per unit by Destination Channel and by Product SKU.

7.  **`Checks` (Quality Audit)**
    
      * **Purpose:** Pre-decision verification list to ensure model accuracy.
      * **Audit Rules:**
          * Confirms product master data (CBM, weight, unit COGS) is present.
          * Verifies unallocated units equal 0 in `Shipment Setup`.
          * Verifies quote validity dates are not expired.
          * Flags Rate Card updates older than 60 days.

8.  **`Shipment Log` (Historical Archive)**
    
      * **Purpose:** Maintains a historical ledger of shipping costs and choices.
      * **Workflow:** Copy values from `Comparison` cells `B28:E28` and paste them into the `Shipment Log` alongside PO number, chosen path, and cost savings realized.-----### 3\. Data Required from Freight Forwarders & 3PLsTo populate **Scenarios 1–3**, request a structured quote breaking down the following line items:
| Category               | Line Item / Metric Needed                                                                       | Applies To   | Notes                                                                            |
| :--------------------- | :---------------------------------------------------------------------------------------------- | :----------- | :------------------------------------------------------------------------------- |
| **Quote Header**       | Quote Reference \#, Expiration Date, Incoterm (`EXW`, `FOB`, `DDP`), Mode (`FCL`, `LCL`, `Air`) | All          | Ensures quote validity and proper tab inputs.                                    |
| **Transit Time**       | Port-to-port transit days + Inland delivery lead time to warehouses                             | All          | Used to calculate days to sellable inventory and cost of capital.                |
| **Origin Charges**     | Factory pickup/trucking, Export Customs clearance, Origin THC/Handling                          | `EXW` only   | Skip for `FOB` / `DDP`.                                                          |
| **Main Freight**       | FCL per container rate, LCL rate per CBM (and min charge), or Air rate per kg                   | `EXW`, `FOB` | For Air, verify volumetric factor (standard $167\\text{ kg/CBM}$).               |
| **Destination Fees**   | Port/Terminal handling (DTHC), Drayage, De-consolidation                                        | `EXW`, `FOB` | Port-to-hub charges at destination.                                              |
| **Customs & Bond**     | Customs brokerage fee, ISF filing, Single entry / Annual Bond fee                               | `EXW`, `FOB` | Billed by customs broker.                                                        |
| **Cargo Insurance**    | Total cargo insurance premium ($)                                                               | `EXW`, `FOB` | Based on invoice value + freight.                                                |
| **Last-Mile Trucking** | Trucking / LTL charges broken down by destination: AWD, FBA Direct, Walmart WFS, TikTok FBT     | `EXW`, `FOB` | Separate costs for each warehouse destination.                                   |
| **3PL Hub Fees**       | Inbound receiving/palletization fees, Monthly storage rate, Outbound prep/transfer fees         | 3PL routing  | Required if using a private 3PL hub instead of AWD.                              |
| **All-In Price**       | Single door-to-door rate per shipment or per unit                                               | `DDP` only   | Includes duty, tariffs, and clearance. Duty inputs are bypassed in the scenario. |

-----### 4\. Step-by-Step Scenario Analysis Workflow#### Step 1: Prepare Master Data1.  Go to `Products`: Check that carton dimensions ($L \\times W \\times H$), carton weights, unit COGS, HTS codes, and duty percentages are populated for all SKUs in the planned order.
2.  Go to `Rate Card`: Verify that Amazon placement fees and AWD storage rates are updated and verified within the last 60 days.#### Step 2: Define Shipment Parameters1.  Go to `Shipment Setup`:
      * Input PO/Shipment Name, Date, and Origin Port.
      * Select product SKUs and total order units.
      * Allocate unit distribution across `To AWD`, `To FBA direct`, `To Walmart WFS`, and `To TikTok FBT`.
      * Verify that `Unallocated units` equals **0**.
      * Choose shared cost allocation basis (`CBM` or `Weight`).
      * Select whether to include Cost of Capital (e.g., $10%$).#### Step 3: Populate Amazon Path (AGL)1.  Go to `Amazon Path (AGL)`:
      * Enter the AGL quote reference, expiration date, transit mode, and main freight rate.
      * Input estimated transit days and storage duration in AWD.#### Step 4: Populate Forwarder Scenarios1.  Open `Scenario 1` (and `Scenario 2` / `Scenario 3` if comparing multiple forwarders):
      * Select `Incoterm` (`EXW`, `FOB`, or `DDP`) and `Mode`.
      * Fill in freight costs, origin charges (if EXW), destination charges (if EXW/FOB), and inland delivery fees for each destination channel.#### Step 5: Run Operational Audit1.  Go to `Checks`: Ensure all check items display **OK**.
2.  If any check displays **CHECK**, **EXPIRED**, or **VERIFY**, return to the indicated tab and resolve the missing or invalid value before making business decisions.#### Step 6: Evaluate Comparative Results1.  Go to `Comparison`:
      * **Cost Comparison:** Review row `27 (TOTAL LANDED COST)` and row `28 (Cost per unit)`.
      * **Savings Analysis:** Check rows `29` and `30` (`Difference vs Amazon path $ / %`) to quantify cost savings against AGL.
      * **Time vs. Cost Trade-off:** Review the **Fastest** vs **Cheapest** flags. If a third-party forwarder is cheaper but takes 15 days longer, evaluate if the savings outweigh the inventory holding cost and stockout risk.
      * **Channel Costing:** Review `COST PER UNIT BY DESTINATION` to determine if certain channels (e.g., FBA Direct) are more economical under specific forwarders.#### Step 7: Log Decision1.  Once a routing path is selected, copy the final landed cost line (`Comparison` cells `B28:E28`).
2.  Paste values into `Shipment Log` alongside the PO name, chosen path, calculated savings, and notes.


