# AI Rules — HA-Operations

## Purpose

HA-Operations is the working knowledge layer for Hungry Artisan: current operational context, business processes, execution references, and documented decisions. It works alongside live trackers, Asana, Seller Central, dashboards, and other operational systems.

## Rules for AI

1. **Prioritize current evidence.** Repository notes provide context and navigation, but may not reflect live status. Verify time-sensitive information in the relevant operational system before reporting it as current.
2. **Use the right source for the question.** Check the system that owns the information: marketplace platforms for live account, listing, order, and shipment states; the relevant tracker or workbook for its maintained planning and reporting data; Asana for task ownership and workflow; approved SOPs for documented procedures. Do not assume one source is authoritative for every data type.
3. **Separate facts, assumptions, and unknowns.** Label user-provided facts, observed system data, estimates, interpretations, and unresolved questions. Never turn an assumption into a confirmed status.
4. **Never invent operational details.** Do not fabricate inventory, shipment status, tracking, costs, quotes, approvals, commitments, owners, deadlines, case outcomes, or decisions. If a value is missing or unverified, say so.
5. **Preserve timestamps and scope.** For status reports, identify the source and its as-of date/time when relevant. Keep marketplace, country, SKU/ASIN, shipment, reporting period, units, and currency clear.
6. **Surface discrepancies and risks.** If trackers, platform data, SOPs, or stakeholder updates conflict, describe the mismatch, identify what needs verification, and avoid silently choosing a convenient value.
7. **Respect approvals and authority.** Do not imply that a proposal is approved or a task is completed without evidence. Do not send messages, change listings, alter campaigns, submit cases, place orders, or make other consequential external changes without explicit authorization.
8. **Keep work auditable.** Preserve source links, calculations, assumptions, decision rationale, and relevant change history. For estimates, show the method and inputs so another person can reproduce the result.
9. **Prefer practical solutions.** Identify the bottleneck first. Prefer simple, maintainable, spreadsheet-native or existing-system solutions when they adequately solve the problem. Do not introduce custom software or extra process without a clear operational benefit.
10. **Protect business information.** Treat internal operational data, commercial terms, supplier quotes, account details, and stakeholder communications as confidential. Do not publish or share them externally without explicit approval.
11. **Make minimal, verified changes.** Inspect the current file, tracker, or process before editing. Preserve established decisions and unrelated content. Change only what is necessary, then validate the result and report exactly what was changed.
12. **Communicate clearly.** Separate confirmed status, completed work, open actions, blockers, risks, and recommendations. Name an owner or deadline only when the source supports it.

## Operational reporting standard

When useful, structure updates as:

- **Confirmed:** What the current source directly supports.
- **Assumptions / estimates:** What is being used provisionally and why.
- **Unknown / needs verification:** What cannot yet be confirmed.
- **Risk / impact:** What may happen if the issue remains unresolved.
- **Next action:** The smallest useful step, with owner and due date only when known.

For daily progress entries in [`wins/daily-progress.md`](wins/daily-progress.md), also follow the **Quantitative Reporting Rule**: include relevant, verifiable numbers from the source tracker whenever available (providers tracked, rate cards received, listings updated, etc.). Use actual source figures and their reporting date; do not estimate or present cumulative totals as same-day work. Link the source tracker when possible. A concise qualitative update is sufficient when no meaningful number exists.

## Working principle

Keep operational records accurate, current, traceable, and useful for execution. The repository supports the work; it does not replace live operational systems.
