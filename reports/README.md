# Reports — Priority Summary & Daily Tracker

> **Purpose:** One lightweight landing page for current operational priorities and a repeatable daily work log. Detailed case/project records and live Google Sheets remain the source of truth.

**Last reviewed:** October 24, 2026  
**Owner:** Wesley Quintero

## Current Priority Summary

Work from the highest operational risk first. Recheck live Seller Center, Asana, email/Slack, and source trackers before changing a status; this summary is a navigation aid, not a replacement for those records.

| Priority | Workstream | Current status | Next action | Detail |
|---|---|---|---|---|
| **P1 — High** | Amazon UK identity verification | Canada reportedly fixed; UK bill document submitted and approval pending. Keep the overall issue open until UK access is confirmed. | Monitor the review; follow up through the existing case if no response arrives within the expected window. | [Case 22710018171](../issues/amazon/22710018171.md) · [Asana](https://app.asana.com/1/1211857003594679/project/1213836032340905/task/1219691863404595) |
| **P1 — High** | Walmart seller-fulfillment suppression | Plan of Action submitted; awaiting Walmart response. WFS transition and submission do not prove the suppression is cleared. | Monitor case 16739258; respond to any follow-up with Justin and confirm the suppression is lifted before closure. | [Case 16739258](../issues/walmart/16739258.md) · [Asana](https://app.asana.com/1/1211857003594679/project/1218837550901608/task/1219444097923296?focus=true) |
| **P1 — High** | TikTok FBT / Estes appointment | Support clarified the process; the specific shipment appointment and SOP update remain open. | Verify appointment with Estes for reference AMC0015150, then update the FBT inbound SOP. | [Ticket & follow-up](../issues/tiktok-shop/202610211812500237.md) · [Estes tracking](https://www.estes-express.com/myestes/shipment-tracking/?type=PO&query=AMC0015150) |
| **P1 — Milestone** | R6 logistics optimization | Initial outreach started; Tactical acknowledged the RFQ and Flexport discovery occurred. Workbook audit is complete; comparable quotes and current provider status still need confirmation. | Check existing correspondence, follow up only where needed, and obtain comparable itemized quotes for China→US, CA, and UK. | [R6 brief](../projects/R6-logistics-optimization.md) · [Progress log](../projects/R6-update-log.md) · [RFQ playbook](../projects/freight-forwarder-rfq-request-playbook.md) · [Workbook audit](../projects/shipment-comparison-workbook-audit.md) |
| **P2 — Medium** | TikTok auto-created inbound reconciliation | Support traced order creation to merchant-configured automation; inventory discrepancy remains unresolved. | Review original inbound order and NCI ticket; reconcile 18 planned, 0 FC-received, and 12 additionally reconciled units before taking shipment/appointment action. | [Ticket record](../issues/tiktok-shop/202610221812500220.md) · [Asana](https://app.asana.com/1/1211857003594679/project/1213836032340905/task/1219792372853538?focus=true) |
| **P2 — Time-sensitive** | Listing Change Calendar / A-B tests | Draft notes flag schedule and asset dependencies that require confirmation against the live sheet. | Confirm actual status or revised dates for T-001/T-002; resolve the T-003/T-004 overlap with the R2 Classic CTR measurement window; confirm creative and pricing separation for upcoming rotations. | [Calendar draft](../a/b-test/listing-change-calendar.md) · [Live calendar](https://docs.google.com/spreadsheets/d/1L5jMrKAYBrO1Q6lrg1fdAKKjkiDS3jgxw6F9STgmD7g/edit?gid=101#gid=101) |
| **Recurring** | Weekly Operations Report | Monday reporting cadence; confirm the team's expected deadline because prior notes reference both 8 AM and 9 AM EST. | Refresh marketplace health, inventory, cases, A/B tests/creative, logistics, and decisions needed; confirm deadline with Victoria if still unclear. | [Weekly ops meeting/report template](./weekly-ops-meeting.md) · [Reporting Hub](https://docs.google.com/spreadsheets/d/14RJd1ChEe8JbpyNPA4x30BNR7VysFLEpLHQUpjElOKs/edit?gid=926197460#gid=926197460) |

### Calendar / listing change watch

- **T-001 / T-002:** Planned start was October 19, 2026, which has passed. Confirm whether these launched; otherwise revise dates and document the reason.
- **T-003 / T-004:** Planned A+ work starts November 2 and may overlap the R2 Classic CTR measurement window ending November 15. Confirm the test window and measurement plan before launch.
- **T-010:** Compact A+ work is planned for October 26–November 15. Confirm creative readiness and reconcile timing against the 7,080 AWD units referenced in the draft.
- **T-011 / T-012:** November mashed-potato image rotations depend on creative being produced and approved.
- **T-005:** December coupon/price activity must not overlap a listing change.
- **T-013 / T-014:** Confirm cranberry creative and reconcile December timing with Black Friday/Cyber Monday and pricing activity.
- **T-008 / T-009:** June 2027 tomato-season timing is an assumption; confirm it before treating the dates as committed.

**Listing-change guardrails:** one listing change per product at a time; do not overlap price/coupon changes with listing changes; do not launch asset-dependent work before creative approval. Nox-suggested dates are proposals, not commitments. Compact is an update project (read before/after), not an A/B test, because traffic is too low. Record baseline, result, lift, decision, learning, and proof link.

## Daily Tracker

Add one dated row per working day. Keep entries short and outcome-focused; link to the detailed record instead of copying the full investigation here. Use **Blocked** when an external response or decision is required, and distinguish work completed from work merely planned.

| Date | Today's top priorities | Completed / outcome | Blocker or decision needed | Next action / owner | Status |
|---|---|---|---|---|---|
| YYYY-MM-DD | 1.  2.  3. |  |  |  | In progress |
| YYYY-MM-DD | 1.  2.  3. |  |  |  | In progress |
| YYYY-MM-DD | 1.  2.  3. |  |  |  | In progress |

### Daily close-out checklist

- [ ] Check urgent marketplace/account-health alerts and active high-priority cases.
- [ ] Review inbound shipments, receiving movement, inventory discrepancies, and required appointments.
- [ ] Check time-sensitive listing tests, creative dependencies, and price/promo conflicts.
- [ ] Move the most important R6 logistics follow-up forward and update the project log only when progress or a blocker materially changes.
- [ ] Record completed outcomes, decisions needed, owner, and next action.
- [ ] Update linked source trackers/case files where the underlying status changed.

### Weekly reporting checklist

- [ ] Account health and listing suppressions across relevant marketplaces.
- [ ] Inventory cover, inbound shipment status, receiving/check-in exceptions, and stranded/unfulfillable items.
- [ ] Support case status, aging, and decisions or evidence needed.
- [ ] A/B test status, creative readiness, and documented results/learnings.
- [ ] Forwarder outreach, comparable quotes, logistics risks, and R6 milestone status.
- [ ] Clear requests for GM/CEO decisions.

## Source-of-Truth Rules

1. **Live trackers and platform records outrank this summary.** Verify before acting.
2. **Do not guess or silently resolve gaps.** Mark data as unknown/unconfirmed and identify who can confirm it.
3. **A support reply is not always operational closure.** Verify the real-world outcome (access restored, suppression lifted, appointment booked, units reconciled).
4. **Avoid duplicate records.** Keep detailed evidence in the relevant case/project file and link to it here.
5. **Update this page when priorities or next actions materially change**, not for every minor message.
