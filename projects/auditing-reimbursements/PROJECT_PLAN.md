# Auditing & Reimbursements — Project Plan

> **Status:** Not yet started — preparation and prototype planning  
> **Pilot marketplace:** Amazon US  
> **Working environment:** Google Sheets + raw exports  
> **Owner:** Wesley (prototype preparation; formal ownership and operational scope to be confirmed)

## 1. Purpose

Prepare and test a practical in-house reimbursement audit methodology using existing Amazon and provider exports. The immediate deliverable is a small, auditable Google Sheets prototype—not a production system.

The project should establish whether the available data is sufficient to independently identify discrepancies, track claim outcomes, verify financial recovery, and evaluate provider fees.

## 2. Outcomes

1. A documented list of required source exports and their limitations.
2. A normalized audit ledger with traceable source references.
3. A repeatable process for identifying and validating potential reimbursement opportunities.
4. A reconciliation method for matching Amazon reimbursement records to financial credits and reversals.
5. A fee review that distinguishes invoice observations from verified contractual billing terms.
6. A short pilot findings report with gaps, exceptions, and recommendations.

## 3. Phased plan

### Phase 0 — Preparation and access check

- [ ] Confirm which Amazon US reports can be exported with current Seller Central access.
- [ ] Obtain sample Inventory Ledger and Reimbursements Report exports.
- [ ] Obtain inbound shipment records for the same sample period, if available.
- [ ] Obtain settlement/transaction records needed to verify credits and reversals.
- [ ] Obtain provider claim export and invoice/fee documentation, if available.
- [ ] Record report names, date coverage, export dates, columns, and access limitations.
- [ ] Keep source exports in an approved, access-controlled location; do not place sensitive raw exports in this repository.

**Exit condition:** A small, documented sample set is available, or specific data gaps are recorded.

### Phase 1 — Google Sheets structure

- [ ] Create the workbook with provisional tabs: `Raw_Imports`, `Audit_Ledger`, `Reconciliation`, `Fee_Audit`, and `Summary`.
- [ ] Define an import register: marketplace, report type, reporting period, export date, source filename, and notes.
- [ ] Inspect actual export schemas before finalizing field mappings.
- [ ] Define a stable record key where possible; retain original Amazon/provider identifiers.
- [ ] Keep raw source data separate from normalized and calculated fields.

**Exit condition:** A sample can be imported and traced from the working ledger back to its source.

### Phase 2 — Normalize and identify

- [ ] Map source fields into a common ledger structure.
- [ ] Define audit categories: missing inbound, warehouse lost, warehouse damaged, customer return/adjustment, reimbursement reversal, customer-service adjustment, and fee discrepancy.
- [ ] Define statuses separately: Potential, Validating, Validated, Submitted, Approved, Paid, Reversed, Rejected/Not Eligible, and Closed.
- [ ] Record evidence, quantity, amount, relevant dates/deadlines, identifiers, and source references.
- [ ] Flag duplicates and incomplete records for review rather than silently dropping them.
- [ ] Document category-specific validation rules only after confirming the applicable Amazon policy and source evidence.

**Exit condition:** Each flagged sample record has a documented reason, status, and source trail.

### Phase 3 — Reconcile financial outcomes

- [ ] Match provider claim references to Amazon reimbursement records where identifiers permit.
- [ ] Match reimbursement records to settlement/transaction credits where the available exports permit.
- [ ] Identify reversals, duplicate reimbursements, unmatched claims, and timing differences.
- [ ] Separate approved amounts from confirmed financial credits.
- [ ] Record unmatched or ambiguous cases as exceptions for manual review.

**Exit condition:** The pilot can distinguish claim status from confirmed financial recovery and explain unmatched records.

### Phase 4 — Provider fee review

- [ ] Capture provider invoice line items and relevant claim references.
- [ ] Obtain the applicable signed agreement or written fee terms before treating a fee rate as contractual.
- [ ] Recalculate fees against the documented billing basis.
- [ ] Compare gross recovery, provider fees, adjustments/reversals, and net recovery only across comparable records and periods.
- [ ] Treat any observed invoice rate as invoice-specific until the governing agreement and calculation basis are verified.

**Exit condition:** Fee calculations are reproducible and their assumptions are documented.

### Phase 5 — Pilot review and recommendation

- [ ] Summarize sample size, date coverage, categories, and data limitations.
- [ ] Report potential opportunities separately from validated claims and confirmed credits.
- [ ] Quantify matched, unmatched, reversed, and unresolved records where evidence supports it.
- [ ] Document manual effort and recurring bottlenecks.
- [ ] Recommend whether to stop, improve the Sheets prototype, or test a small automation.
- [ ] Obtain management alignment before treating the prototype as an ongoing operational responsibility.

**Exit condition:** A concise findings report supports a clear next-step decision.

## 4. Proposed audit ledger fields

Finalize these only after inspecting the real exports.

| Field group | Candidate fields |
|---|---|
| Record identity | Audit ID, marketplace, audit category, status |
| Product | SKU, ASIN, FNSKU, product title (if available) |
| Event reference | Shipment ID, order ID, claim ID, reimbursement ID, transaction ID |
| Dates | Event date, discovery date, claim submission date, reimbursement date, reversal date, applicable deadline |
| Quantity | Expected units, received units, discrepancy units, reimbursed units |
| Amounts | Potential amount, submitted amount, approved amount, paid/credited amount, reversed amount |
| Provider | Provider name, provider claim reference, fee basis, fee rate, fee amount |
| Reconciliation | Match status, match reference, exception reason |
| Evidence | Source filename, source row/reference, evidence location, reviewer notes |
| Control | Created date, last reviewed date, next action, owner |

Do not assume every field exists in every export. Preserve source-specific identifiers and leave unavailable fields blank with a documented reason.

## 5. Key controls and definitions

- **Potential opportunity:** A discrepancy that warrants investigation; not yet proof of Amazon liability.
- **Validated:** Supporting evidence and applicable policy review justify pursuing the discrepancy.
- **Submitted:** A claim or case has actually been filed and has a reference.
- **Approved:** Amazon/provider reports an approved outcome; not by itself proof of a financial credit.
- **Paid/credited:** Financial activity confirms the reimbursement credit.
- **Reversed:** A previously recorded reimbursement was later offset or taken back.
- **Net recovery:** Confirmed credits less confirmed reversals and applicable provider fees, using a clearly stated period and fee basis.
- **Missing data:** Unknown, not zero. Keep exceptions visible.
- **Duplicate control:** Do not count the same event or recovery more than once.

## 6. Risks and dependencies

| Risk / dependency | Handling |
|---|---|
| Missing report access or limited history | Record coverage and request only the access needed |
| Export schemas differ by marketplace/report version | Inspect and map each source before formulas are finalized |
| Inconsistent claim identifiers | Use multiple corroborating fields and retain manual exception review |
| Approval mistaken for cash recovery | Require financial transaction evidence for paid/credited status |
| Reversals or duplicate records | Maintain separate reversal and duplicate checks |
| Unverified provider fee assumptions | Obtain governing agreement and reconcile invoice calculations |
| Sensitive Seller Central data | Keep raw files out of GitHub; use approved secure storage |
| Prototype becomes assumed ongoing ownership | Confirm scope, capacity, and management expectations before operational rollout |

## 7. Out of scope for this preparation phase

- SP-API integration or scheduled data ingestion
- Automated case creation or claim submission
- Production-scale in-house reimbursement operations
- Provider termination or replacement recommendation
- React dashboard, backend, database, or hosting
- Expansion to CA/UK before the US pilot is validated

These may be considered later only if the pilot demonstrates a real bottleneck that warrants the added maintenance.

## 8. Decision gate

At the end of the pilot, choose one:

1. **Stop:** Data quality, recoverable value, or effort does not justify further work.
2. **Continue with Sheets:** The manual process is useful and remains manageable.
3. **Automate a narrow step:** A repetitive, validated bottleneck justifies a small formula/script/API experiment.
4. **Propose formal operational scope:** Management reviews ownership, time allocation, access, controls, and expected outcomes before ongoing execution.

## 9. Progress log

| Date | Update | Evidence / decision |
|---|---|---|
| 2026-11-11 | Created project folder, README, and preparation plan. | Initial scope set to Amazon US + Google Sheets + raw exports. |

---

**Working rule:** Validate the data and reconciliation method first. Build only what the proven process needs.
