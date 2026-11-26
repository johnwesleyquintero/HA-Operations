# R6 Recovery — AGL + AWD Cost Comparison

**Owner:** Wesley  
**Purpose:** Give Justin a clear cost comparison of the current AGL + AWD setup versus using independent logistics.

## Main question

**If HA moves away from AGL and AWD, what would it cost to move inventory from China to Amazon FBA independently?**

No routing change is being recommended or approved. This is a cost investigation only.

## Minimum actionable steps

### 1. Establish the current cost
- [ ] Pull a recent representative shipment and its AGL charges.
- [ ] Capture the related AWD storage, handling, and replenishment costs.
- [ ] Record any AGL discounts or Amazon placement-fee benefits that apply.
- [ ] Record the shipment origin, destination, units, and volume for a later like-for-like comparison.

**Output:** Current AGL + AWD cost baseline.

### 2. Collect provider pricing and service information
This stage is a general rate-card and pricing-sheet collection exercise, **not a shipment-specific RFQ**. We do not need to lock every destination or shipment assumption before making the initial requests.

- [ ] Contact existing providers and ask for their latest pricing sheets/rate cards as part of HA's logistics-system update.
- [ ] Contact new provider candidates and explain that HA is looking for potential logistics partners; ask for their service coverage, capabilities, and pricing.
- [ ] For 3PLs, collect rates for receiving, unloading, storage, handling, and outbound shipping where available.
- [ ] For freight providers, collect their current rate sheets, service lanes, coverage, and a breakdown of included and excluded charges.
- [ ] Track who has been contacted, what was received, and what still needs follow-up.

**Output:** Current pricing sheets, rate cards, service details, and provider coverage information.

### 3. Confirm relevant shipping scenarios
- [ ] Use the geographic sales analysis as an input when identifying relevant regions.
- [ ] Validate destination assumptions against Amazon's actual inbound/placement requirements, provider coverage, and available 3PL locations.
- [ ] Once the scenarios are clear, request any destination- or shipment-specific pricing needed to complete the comparison.

Possible routes to evaluate:

- **Direct to FBA:** China → independent forwarder → FBA.
- **Via 3PL:** China → independent forwarder → 3PL → FBA.

**Output:** Agreed comparison scenarios and any additional pricing needed for those specific routes.

### 4. Compare and report
- [ ] Compare current AGL + AWD against each feasible independent route.
- [ ] Show total cost and cost per unit using equivalent shipment assumptions.
- [ ] Include applicable origin charges, freight, customs, destination charges, drayage, receiving/unloading, storage, handling, outbound transportation, and Amazon inbound/placement fees.
- [ ] Identify missing quotes, assumptions, excluded fees, and operational trade-offs.
- [ ] Share the cost difference and findings with Justin.

**Output:** Simple side-by-side comparison showing the current model against independent alternatives.

## Provider list

| Provider | Initial request | Status | Pricing record |
|---|---|---|---|
| Rivera | Current freight pricing sheet, service lanes, and charge breakdown | Requested | Awaiting response |
| Flexport | Current freight pricing sheet, service lanes, and charge breakdown | Not requested | — |
| Tactical Logistic Solutions | Current freight pricing sheet, service lanes, and charge breakdown | Not requested | — |
| 3PL Guys | Updated 3PL rates for receiving, unloading, storage, handling, and outbound shipping | Pricing received — under review | [3PL Guys pricing sheet](3pl-guys-pricing.md) |
| Other existing 3PLs | Updated pricing sheet/rate card and service coverage | Not requested | — |
| New 3PL candidates | Service overview, coverage, capabilities, and pricing sheet | Not requested | — |

## Provider outreach messages

Keep the messages short and natural. The goal at this stage is to collect current pricing and understand provider capabilities, not to send a formal shipment RFQ.

### A. Existing 3PL provider — request updated rates

**Subject:** Updated Pricing

Hi [Name],

We're updating our logistics rates and reviewing our current setup. Can you send over your latest pricing sheet, including any updated rates for receiving, unloading, storage, handling, and outbound shipping?

If there have been any changes to your services or coverage, please include those as well.

Thanks,  
Wesley  
Hungry Artisan

### B. New 3PL candidate — introduce HA and request pricing

**Subject:** 3PL Services and Pricing

Hi [Name],

I'm with Hungry Artisan. We're looking at adding logistics partners and would like to learn more about your 3PL services.

Can you send over your pricing sheet and a quick overview of your services and warehouse locations? We're particularly interested in receiving, unloading, storage, handling, and shipping inventory out to Amazon FBA.

Thanks,  
Wesley  
Hungry Artisan

## Comparison rule

Use the same shipment details for both models wherever possible. Do not compare freight-only rates against an all-in AGL + AWD cost. Separate confirmed charges from estimates and unknowns. General rate sheets are useful for initial screening, but confirm validity, lane, volume assumptions, accessorials, and exclusions before using rates in the final cost comparison.

## Out of scope for this recovery pass

- Building a full multi-country logistics strategy.
- Creating a new ongoing multi-forwarder procurement system.
- Executing a shipment or changing current routing.
- Treating a general rate sheet as a final, shipment-specific quote.
- Expanding the 3PL search beyond the initial pricing review unless the rates or coverage show a clear need.

**Definition of done:** Justin receives a like-for-like cost comparison showing what the current AGL + AWD model costs, what an independent alternative is estimated to cost, and what information is still missing.
