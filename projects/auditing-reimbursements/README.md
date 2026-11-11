# Auditing & Reimbursements

> **Status:** Preparation / prototype planning  
> **Initial scope:** Amazon US, Google Sheets, and raw marketplace/provider exports  
> **Purpose:** Establish a repeatable, evidence-based in-house reimbursement audit method before considering automation or a broader operational rollout.

## Objective

Build and validate a lightweight audit workflow that can identify potential reimbursement discrepancies, document supporting evidence, track claim outcomes, reconcile Amazon credits and reversals, and calculate net recovery after provider fees.

This is an exploratory preparation project. It does **not** establish a formal commitment to replace an external reimbursement provider, submit claims at scale, or build a software application.

## Working principles

- Start with raw exports and Google Sheets; do not assume API access.
- Preserve source exports unchanged and make every working record traceable to its source.
- Separate potential opportunities from validated, submitted, approved, paid, reversed, and closed records.
- Treat Amazon financial records as the evidence for credits and reversals; an approval or provider status alone is not proof of cash recovery.
- Record unknowns and data gaps explicitly. Never convert missing information into zero or an assumed outcome.
- Keep formulas and audit rules visible and reviewable.
- Validate the process manually before introducing Apps Script, APIs, databases, or a React interface.
- Compare provider fees and net recovery only when the underlying records and billing basis are sufficiently comparable.

## Initial workflow

1. **Import** — Save original Amazon and provider exports in a controlled source folder; record marketplace, report type, date range, export date, and filename.
2. **Normalize** — Map relevant source fields into a consistent audit ledger without altering the raw data.
3. **Identify** — Flag possible discrepancies such as missing inbound units, warehouse lost/damaged inventory, customer-return adjustments, reimbursement reversals, and fee discrepancies.
4. **Validate** — Check eligibility, timing, quantities, identifiers, evidence, and potential duplicate claims.
5. **Track** — Record claim submission and status changes with references and dates.
6. **Reconcile** — Match Amazon reimbursement records to settlement/transaction evidence; identify reversals and unmatched records.
7. **Calculate** — Determine gross confirmed recovery, provider fees, and net recovery using a verified fee basis.
8. **Review** — Summarize findings, exceptions, unresolved questions, and recommended next actions.

## Proposed Google Sheets workbook

| Tab | Purpose |
|---|---|
| `Raw_Imports` | Import register and/or staging area for source exports; preserve original values |
| `Audit_Ledger` | Normalized record-level audit register |
| `Reconciliation` | Match claims and reimbursement records to Amazon financial activity |
| `Fee_Audit` | Review provider invoices, fee basis, charges, and net recovery |
| `Summary` | Aggregate opportunities, claim statuses, confirmed credits, reversals, fees, and exceptions |

The workbook structure is provisional and should be adjusted to the actual columns and limitations of the available exports.

## Initial source data

Start with Amazon US and a limited date range. Obtain whichever of the following are available:

- Inventory Ledger
- Reimbursements Report
- FBA inbound shipment / shipment contents records
- Settlement or transaction records that show reimbursement credits and reversals
- Provider claim export (e.g., Threecolts), if available
- Provider invoice and applicable fee agreement/rate documentation

Do not assume every report is available for every marketplace, date range, or account role. Record report coverage and limitations during the test.

## Scope boundaries

**Included in the initial prototype**
- Amazon US sample
- Raw CSV/XLSX exports
- Google Sheets-based normalization and reconciliation
- Manual evidence review and documented exceptions
- Basic recovery and fee calculations

**Not included yet**
- Automated SP-API integration
- Automated claim submission
- Production reimbursement operations or provider replacement
- React dashboard, database, or hosted application
- Multi-marketplace rollout
- Claims or financial conclusions unsupported by source evidence

## Success criteria

The prototype is useful when we can:

- Trace each normalized record to its original source file and source row/reference.
- Explain why a record was flagged as a potential opportunity.
- Distinguish a potential discrepancy from a validated claim and a confirmed financial recovery.
- Identify duplicate, unmatched, reversed, and unresolved records.
- Reconcile confirmed reimbursement credits to Amazon financial activity where the exports permit.
- Calculate provider fees and net recovery using a documented, verified fee basis.
- State the limits of the sample, report coverage, and any assumptions.

## Project documents

- [Project Plan](./PROJECT_PLAN.md)

## Important note

This repository documents the preparation methodology and project progress. Do not commit raw Seller Central exports, customer personal information, credentials, access tokens, or other sensitive account data. Store source files only in an approved, access-controlled location and use sanitized samples in this repository when documentation requires examples.
