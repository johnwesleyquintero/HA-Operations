# Reimbursement Operating Model Benchmark

> **Purpose:** Compare managing Amazon reimbursement work in-house against external providers, beginning with Threecolts and the former GETIDA relationship.  
> **Status:** Initial benchmark — evidence gathering required  
> **Prepared from:** Justin Hopkins' November 5–10, 2026 email thread and Threecolts invoice `VIJW7PDB-0012` dated November 4, 2026.

## 1. Why this comparison exists

On November 5, 2026, Justin forwarded a Threecolts invoice and asked whether we were familiar with the service, noting that some brands manage reimbursement work in-house.

Wesley replied on November 10 asking whether the longer-term intention was to move away from Threecolts and manage the process internally.

Justin clarified on November 10:

> “I may want to bring this in house down the road, but for now I’d like to get more clarity on the process and related expense so we can compare to GETIDA, other companies or doing it ourselves. I am very unfamiliar with process and how they are charging. It seems many teams bring in-house and I don’t know what that entails or the related savings to be able to determine if we should.”

### Management intent

The immediate request is **not to replace Threecolts now**. Justin wants visibility into:

1. What the reimbursement process actually involves.
2. What Threecolts is doing for Hungry Artisan and what work is included.
3. How the provider charges and what the total expense represents.
4. How the current arrangement compares with the former GETIDA arrangement and other providers.
5. What tasks, skills, tools, time, controls, and costs would be required to manage the process in-house.
6. Whether any potential savings justify the operational effort and risk.

The current project is therefore a fact-finding and benchmarking exercise. The Google Sheets prototype is intended to make the work and economics visible before any operating-model decision is made.

## 2. Operating model comparison

| Dimension | In-house | Threecolts | GETIDA |
|---|---|---|---|
| Operating model | HA staff identify, validate, submit, monitor, reconcile, and audit reimbursement claims. | External reimbursement service/provider performs some or all agreed reimbursement work. Exact HA scope must be confirmed. | Former external reimbursement provider. Historical scope and current/previous HA terms need confirmation. |
| How it charges | No provider success-fee percentage by default, but not free. Cost is internal labor plus any software, training, administration, and oversight. | HA's November 4, 2026 invoice explicitly shows a **20% billing rate** on the listed reimbursement amounts. Confirm this against the signed agreement and full billing rules. | **Not yet verified for HA.** Obtain the prior agreement and invoices to establish the actual rate, billing basis, minimums, exclusions, and any other fees. |
| Cost basis | Hours spent × loaded labor rate, plus attributable tools and overhead. | Invoice-specific evidence indicates 20% of listed reimbursement amounts. Confirm whether the rate applies to all recovery types and when fees are triggered. | Unknown until historical contract/invoice review. Do not assume it matches Threecolts or a public advertised rate. |
| Work performed | HA owns the entire workflow and quality controls. | Provider scope, automation, claim coverage, exclusions, and HA responsibilities need to be documented from contract and workflow evidence. | Historical service scope needs to be recovered from prior records, agreement, and invoices. |
| Visibility / control | Direct control over data, prioritization, and audit decisions; requires internal SOPs and quality assurance. | Depends on provider reporting, access, export detail, and contract. | Depends on historical provider reporting and contract. |
| Main trade-off | Potential fee savings and stronger internal knowledge, in exchange for staff time, training, process ownership, and execution risk. | Outsourced expertise and reduced internal workload, in exchange for provider fees and dependency on provider visibility/performance. | Same general outsourced-versus-in-house trade-off; actual value cannot be assessed until HA's historical terms and results are reviewed. |
| Evidence needed | Pilot time tracking, repeatable SOP, sample audit results, staffing cost, and tooling needs. | Signed agreement, invoices, claim exports, claim status history, fee calculations, and actual Amazon financial outcomes. | Prior agreement, invoices, claim exports, fee calculations, and actual Amazon financial outcomes. |

### Pricing status at a glance

- **In-house:** No vendor commission is assumed, but calculate the full internal cost. Staff time is a real cost.
- **Threecolts:** 20% is directly shown as the billing rate on the supplied November 4 invoice. It is an observed invoice rate, not yet a verified statement of every contractual term.
- **GETIDA:** HA-specific pricing is currently unknown. Retrieve historical documentation before entering a rate or comparing savings.

Do not insert generic internet pricing or another seller's negotiated rate as if it were HA's actual price.

## 3. Threecolts invoice — observed cost example

### Invoice details

| Item | Invoice evidence |
|---|---|
| Provider | Threecolts |
| Invoice number | `VIJW7PDB-0012` |
| Invoice date | November 4, 2026 |
| Due date | November 7, 2026 |
| Customer memo | Enriched Products, LLC (ID: 849207) |
| Total due | **$529.69** |
| Amount paid shown on invoice | **$0.00** |
| Amount remaining shown on invoice | **$529.69** |
| Billing rate shown on listed records | **20%** |

The supplied invoice lists reimbursement entries with reasons including `Lost_Inbound` and `Damaged_Warehouse`. Each listed entry displays a 20% billing rate and a line subtotal calculated as the reimbursement amount multiplied by 20%.

At a 20% rate, the invoice's $529.69 fee corresponds mathematically to **$2,648.45 in billed reimbursement value** if all line items use the displayed rate and there are no other adjustments. This is an arithmetic implication of the invoice, not an independent confirmation that all $2,648.45 was successfully credited and retained by Amazon.

### Important audit observations

- The invoice shows an amount due and $0.00 paid at the time represented by the invoice. It does not prove the invoice was later paid.
- The provider invoice is evidence of provider billing, not by itself proof that each reimbursement was successfully credited and retained.
- Reconcile each reimbursement ID against Amazon's reimbursement records and settlement/transaction activity.
- Check for reversals, duplicate records, and differences between the provider's billed amount and Amazon's final financial outcome.
- The invoice contains two line entries with reimbursement ID `23544407531` for different SKUs/FNSKUs. Preserve the provider line IDs and investigate the relationship rather than assuming either a duplicate charge or two independent reimbursements.
- The invoice's displayed line quantity is not a substitute for checking the reimbursed unit quantity in the underlying records.

## 4. What in-house work would actually entail

An in-house process is more than downloading a report and opening Amazon cases. HA would need to own the complete control cycle:

1. **Data collection** — Download and retain the required Amazon reports and relevant provider/financial exports on a defined schedule.
2. **Opportunity identification** — Find potential discrepancies in inbound shipments, warehouse inventory events, returns/adjustments, reimbursements, and reversals.
3. **Eligibility and evidence review** — Check identifiers, shipment/order history, timelines, quantities, policy requirements, and supporting evidence.
4. **Claim preparation and submission** — Prepare the appropriate case or claim and retain its reference and submission evidence.
5. **Follow-up** — Monitor responses, requests for evidence, denials, approvals, and unresolved cases.
6. **Financial reconciliation** — Verify reimbursement credits and reversals against Amazon financial records.
7. **Provider/fee audit** — Reconcile external provider claims and invoice charges where applicable.
8. **Reporting and controls** — Track gross recovery, confirmed reversals, provider fees, net recovery, aging, exceptions, and audit completeness.

### Required operating capabilities

- Seller Central access and familiarity with the relevant reports and claim workflows.
- Understanding of reimbursement categories, eligibility rules, and claim deadlines.
- Spreadsheet-based data normalization and reconciliation.
- Evidence retention and case tracking.
- Financial transaction reconciliation.
- Quality checks for duplicate claims, reversals, and unsupported claims.
- Defined ownership, backup coverage, and review cadence.

A single person may be able to run a small process, but capacity should be measured during a pilot rather than assumed.

## 5. How to compare the economics fairly

Use the same marketplace, period, claim categories, and financial outcome definitions for all models.

### Core calculations

**Provider cost**
`Provider fees actually invoiced for the comparable cohort`

**In-house operating cost**
`Staff hours × loaded hourly cost + attributable tools/training/overhead`

**Confirmed net recovery**
`Amazon credits confirmed − confirmed reversals − provider fees`

For in-house, there is no external provider fee in the formula, but internal operating cost must still be accounted for when comparing the economics.

**Net value after operating cost**
`Confirmed Amazon credits − reversals − provider fees − internal operating cost`

Avoid comparing a provider's approved-claim value with in-house paid recovery. Compare like with like, preferably using confirmed financial credits net of reversals.

### Suggested comparison measures

| Measure | Why it matters |
|---|---|
| Potential opportunities identified | Shows detection coverage, not recovered money |
| Claims validated and submitted | Shows actionable workload |
| Confirmed reimbursement credits | Measures actual financial recovery |
| Reversals / offsets | Prevents overstating recovery |
| Provider fees | Measures outsourced service cost |
| Internal hours | Measures in-house workload |
| Internal cost | Converts workload into comparable economics |
| Net recovery after fees/cost | Supports the operating-model decision |
| Unmatched / unresolved records | Shows data quality and process risk |
| Recovery per labor hour | Helps assess internal process productivity |

## 6. Evidence and open questions

### Threecolts

- [ ] Obtain the signed agreement / order form and verify the contractual fee rate and billing trigger.
- [ ] Confirm which reimbursement categories and marketplaces are covered.
- [ ] Confirm whether fees apply to cash reimbursements, inventory reimbursements, or both.
- [ ] Confirm how reversals, duplicate reimbursements, refunds, and later adjustments are handled.
- [ ] Obtain detailed claim export with provider IDs, Amazon reimbursement IDs, dates, statuses, and billed amounts.
- [ ] Reconcile invoice line items to Amazon financial records.
- [ ] Confirm payment status of invoice `VIJW7PDB-0012` from the accounting/payment record.

### GETIDA

- [ ] Retrieve HA's former GETIDA agreement and pricing schedule.
- [ ] Retrieve representative invoices and claim-level billing exports.
- [ ] Confirm actual fee rate, fee basis, billing trigger, minimums, exclusions, and any additional charges.
- [ ] Establish the period of service and whether the historical data is comparable to the Threecolts sample.
- [ ] Compare confirmed net recovery, not only gross claim values or invoice percentages.

### In-house

- [ ] Identify the exact reports and Seller Central permissions available to HA.
- [ ] Run a limited Amazon US sample in Google Sheets.
- [ ] Track time spent importing, investigating, submitting, following up, and reconciling.
- [ ] Document the SOP, exception handling, review controls, and backup coverage needed.
- [ ] Estimate internal cost using an agreed loaded labor rate.
- [ ] Identify which tasks could be simplified or automated only after the manual workflow is validated.

## 7. Recommended next steps

1. **Understand Threecolts first:** Map its workflow, deliverables, claim coverage, and billing from the actual HA records.
2. **Recover GETIDA evidence:** Use the prior agreement and invoices to establish HA's historical pricing and service scope.
3. **Build the in-house baseline:** Use raw Amazon exports and a Google Sheets prototype for one controlled US sample.
4. **Track labor and outcomes:** Record effort and reconcile confirmed credits, reversals, fees, and exceptions.
5. **Prepare a decision comparison:** Present the economics, workload, risks, and data gaps to Justin.
6. **Make no provider-change assumption:** Any move in-house should be a separate management decision after the evidence is reviewed.

## 8. Current conclusion

The November 4 Threecolts invoice provides an initial, concrete example of a **20% billing rate** and a **$529.69 invoice**. It does not establish the full contract terms, the provider's complete scope, or the final net recovery after any reversals.

GETIDA's actual HA pricing is not yet documented in the evidence available for this benchmark. In-house cost is also not zero; it must be measured as labor and operating expense.

The right next step is to compare all three models using the same source records and confirmed financial outcomes. The purpose is to help Justin make an informed decision—not to presume that bringing the work in-house is automatically cheaper or better.
