# A/B Testing & Listing Change Planning

> **Status:** Internal working reference. The Google Sheet is the live source of truth. This README summarizes the calculated timeline, calendar guardrails, and unscheduled listing-work queue supplied from the Test Calendar and Events tabs. It does not authorize a listing change.

**Live calendar:** [HA Listing Change Calendar](https://docs.google.com/spreadsheets/d/1L5jMrKAYBrO1Q6lrg1fdAKKjkiDS3jgxw6F9STgmD7g/edit?gid=101#gid=101)  
**Supporting calendar notes:** [Listing Change Calendar draft](./listing-change-calendar.md)  
**Creative assets:** [HA Creative & Brand Assets](https://drive.google.com/drive/folders/1cuNij3bOBUQ1-3rsA_3Z6zwgFA2TZTOu)  
**A/B testing recommendations:** [HA A-B Testing Recommendation folder](https://drive.google.com/drive/folders/1VRScy9a-mWKtuKjIPHTOlgBXR56YYwtj)  
**Pricing coordination:** [HA Promo & Pricing Tracker](https://docs.google.com/spreadsheets/d/15lhLdBn4BsS2gDUMA-phiwnq_SxsQZ5tcqHDdI1wPlc/edit?gid=1677883015#gid=1677883015)  
**Promotion review priorities:** [Promo & Pricing Tracker — review deadlines and recommendations](./promo-pricing-tracker.md)

## How to read the timeline

The sheet's **Timeline: What Is Running When** section is calculated from the Test Calendar and Events tabs. **Do not type into the timeline.**

- **Green:** a test/change is running that week.
- **Red:** two tests are scheduled on the same product that week.
- **Amber:** an event or freeze affects that week.
- **Yellow cells:** editable/type-in fields in the planning tabs.
- **Grey cells:** calculated fields.

The timeline is a conflict detector, not an approval mechanism. A row appearing on the timeline does not prove it launched or that its dates remain valid. Confirm actual status in the Test Calendar and resolve red/amber flags before making a change.

## Timeline snapshot from the supplied sheet

Weekly columns supplied: October 12, 2026 through October 4, 2027. This is a transcription of the provided timeline snapshot, not a live recalculation.

| Product | Weeks shown as active | IDs shown |
|---|---|---|
| Classic Food Mill | Oct 19–26, 2026 | T-001 |
| Classic Food Mill | Nov 2–9, 2026 | T-003, T-011 |
| Classic Food Mill | Nov 30–Dec 14, 2026 | T-005, T-013 |
| Classic Food Mill | Jan 4–11, 2027 | T-015 |
| Classic Food Mill | Apr 26–May 10, 2027 | T-006 |
| Classic Food Mill | Jun 28–Jul 12, 2027 | T-008 |
| Premium Food Mill | Oct 19–26, 2026 | T-002 |
| Premium Food Mill | Nov 2–9, 2026 | T-004, T-012 |
| Premium Food Mill | Nov 30–Dec 14, 2026 | T-014 |
| Premium Food Mill | Jan 4–11, 2027 | T-016 |
| Premium Food Mill | Apr 26–May 10, 2027 | T-007 |
| Premium Food Mill | Jun 28–Jul 12, 2027 | T-009 |
| Compact Food Mill | Oct 26–Nov 9, 2026 | T-010 |
| Canning Kit V2 | No active IDs shown in this snapshot | — |

**Interpretation caution:** The source grid labels weeks by their starting dates and places IDs in individual weekly cells. Date ranges above summarize adjacent populated cells; always use the Test Calendar's exact planned start/end dates for scheduling. The timeline snapshot itself should not be treated as confirmation of actual launch dates.

## Events and freezes

| Event / constraint | Weeks shown | Operating implication |
|---|---|---|
| R2: Classic CTR measurement window, through Nov 15, 2026 | Oct 12, Oct 19, Oct 26, Nov 2, Nov 9 | Protect the measurement window. Confirm with the responsible team before introducing changes that could contaminate results. |
| Black Friday / Cyber Monday and BFCM freeze | Nov 16, Nov 23, Nov 30 | No new tests during the stated BFCM freeze. Confirm exact freeze start/end and any approved exceptions in the live sheet. |
| Holiday taper starts | Dec 14, Dec 21, Dec 28 | Treat the holiday taper as a scheduling constraint; confirm what changes are permitted. |

## Listing work waiting to be scheduled

These queue items are not independent instructions to change a listing. When an item is scheduled, assign its Calendar ID in column K and set Status to **Scheduled**. Keep it **Queued** until the date, assets, and dependencies have been reviewed.

| Queue ID | Product | Work | Priority / status | Asset dependency | Calendar link / next action |
|---|---|---|---|---|---|
| **P-001** | Compact Food Mill | Add an A+ image showing the Compact disassembled and stored in a drawer, highlighting the drawer-storage USP. | High · Queued | Photo/render of product pieces in a drawer and one A+ module. Creative owner to confirm. Needed by Nov 30, 2026. | Linked to **T-010**. Set the actual date from the restock timing; aim to complete before the 7,080 AWD units reach FBA. Compact currently has no sales, so document before/after performance rather than calling it an A/B test. |
| **P-002** | Classic Food Mill | Create the November/Thanksgiving mashed-potato main-image set. | High · Queued | Images do not yet exist. Justin owns the change; Alex (Upwork) is listed as asset owner. Needed by Oct 30, 2026. | Linked to **T-011**. Dates are proposals. Confirm asset completion/approval and resolve the overlap with the R2 CTR window before scheduling. |
| **P-003** | Premium Food Mill | Create the November/Thanksgiving mashed-potato main-image set, keeping the silicone handle visible. | High · Queued | Images do not yet exist. Justin owns the change; Alex (Upwork) is listed as asset owner. Needed by Oct 30, 2026. | Linked to **T-012**. Brief Classic and Premium together for a consistent set; confirm asset completion/approval and resolve the measurement-window conflict before scheduling. |

## Calendar items needing review

- **T-001 / T-002:** Planned start October 19, 2026, is in the past. Confirm whether they actually launched. If not, revise the dates and document why.
- **T-003 / T-004:** Planned A+ tests start November 2 while the R2 Classic CTR measurement window runs through November 15. Confirm whether these changes must be deferred to protect the measurement window.
- **T-011 / T-012:** The mashed-potato rotations are asset-blocked until the new image sets exist and are approved; the proposed start also falls within the R2 measurement window.
- **T-010 / P-001:** Confirm creative readiness and use current inbound/restock information to decide timing before the 7,080 AWD units reach FBA. The planned October 26 start is a proposal, not confirmation of launch.
- **T-005:** The December coupon test is a price lever. Do not overlap it with a listing change; reconcile the sheet's price/listing conflict flag before scheduling.
- **T-013 / T-014:** Confirm cranberry-sauce assets and coordinate December dates with BFCM and pricing activity.
- **T-008 / T-009:** June 2027 tomato-season start is an assumption; confirm before treating it as committed.
- **Canning Kit V2:** No active calendar IDs appear in the supplied timeline snapshot. This does not imply no future work is needed; it only records what was shown.

## Non-negotiable planning rules

1. One listing change per product at a time. Resolve same-product overlap flags first.
2. Price/coupon changes must not overlap listing changes. Coordinate with the Promo & Pricing Tracker.
3. Do not launch seasonal changes before the required assets are created, approved, and available.
4. Treat Nox-suggested dates as proposals until Wesley and Mae review them.
5. Keep A/B tests, seasonal rotations, and update projects correctly classified.
6. Compact is an **update project**, not an A/B test, because traffic is currently too low for a reliable experiment. Compare a defined before/after period and disclose other changes that could affect the result.
7. For each completed change, preserve baseline, result, measurement window, lift where appropriate, decision, learning, and proof link.
8. If dates, assets, status, or dependencies are unknown, flag them for confirmation rather than guessing.

## Simple workflow

1. Check the live Test Calendar, Events tab, and calculated timeline.
2. Confirm product, change type, owner, dates, metric, and dependencies.
3. Check same-product overlaps, events/freezes, and price/promo activity.
4. Confirm creative is ready before scheduling asset-dependent work.
5. For queue work, add the Calendar ID and set Status to **Scheduled** only after scheduling is agreed.
6. Record actual start/end and results after launch; keep this README as context, not a duplicate live tracker.

**Source of truth:** The [Google Sheet](https://docs.google.com/spreadsheets/d/1L5jMrKAYBrO1Q6lrg1fdAKKjkiDS3jgxw6F9STgmD7g/edit?gid=101#gid=101). If this document and the live sheet differ, verify the current sheet and update the supporting notes.
