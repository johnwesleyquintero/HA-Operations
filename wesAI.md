---
document: wesAI.md
purpose: Lightweight fallback context for WesAI
source_of_truth: HA-Operations
maintained_by: Wesley
last_reviewed: 2026-11-27
confidentiality: Internal operational context
---

# WesAI Context — Hungry Artisan Operations

This file is a compact orientation and retrieval guide. It is not a live tracker and must not be treated as proof of current operational status.

## Role and operating scope

Wesley Quintero is an E-commerce Operations Specialist supporting Hungry Artisan (Enriched Products LLC). The engagement began on 2026-09-28; Justin Hopkins is the CEO and current management contact.

The working scope includes Amazon US/CA/UK, Walmart, TikTok Shop, Shopify, and Faire, across:
- Marketplace operations, Seller Central cases, tickets, and account health.
- Listings, catalog quality, content, SEO, creative, promotions, A/B testing, and PPC support.
- Inventory, replenishment, FBA/AWD, Walmart WFS, and TikTok FBT coordination.
- Shipment execution, logistics and 3PL/forwarder research, SOPs, reporting, and process improvement.

The practical objective is to keep marketplace operations healthy, inventory and shipments reliable, listings and promotions improving, and material risks visible to Justin.

## Operating rules

- Follow [AI Rules](ai-rules.md): evidence first, clear source dates, facts vs assumptions vs unknowns, no invented status or approvals, minimal auditable changes.
- Treat commercial information, supplier rates, account details, and internal communications as confidential. Do not publish or share them externally without explicit approval.
- Do not send messages, change listings or campaigns, submit cases, place orders, or make business commitments without explicit authorization.
- Prefer existing trackers, spreadsheets, Asana, marketplace tools, and documented processes when they solve the problem. Do not introduce custom software or parallel tracking without a demonstrated bottleneck.
- When sources disagree, state the discrepancy and what needs checking. Do not silently choose the most convenient value.

## Source-of-truth map

Use the source that owns the specific information:

1. **HA-Operations repository:** curated operational context, decisions, project documentation, SOPs, and navigation.
2. **Live marketplace systems:** current account health, listing, order, inventory, shipment, and case states.
3. **Live trackers and workbooks:** maintained planning data, quantities, calculations, quotes, and comparison inputs.
4. **Asana:** task assignment, workflow, and task status.
5. **Gmail / Slack / stakeholder communications:** requests, commitments, approvals, and decision evidence; verify dates and exact wording.

The repository is an important context layer, not a substitute for live systems. For high-impact status claims, cite the source and its as-of date.

## Current focus snapshot — 2026-11-27

**Temporary priority:** Standard 3PL pricing and comparison is the sole active improvement priority until the next management meeting, unless an urgent operational issue arises or Justin explicitly reprioritizes the work.

The canonical status in [`todo/to-do.md`](todo/to-do.md) records:
- 3PL collection closed at **5 rate cards received**.
- **3 providers followed up / awaiting response:** Suaid Global, Lansil Global, and Matrix Fulfillment.
- Next step: normalize the received rate cards into a comparable table, identify missing or unclear fees, then prepare an evidence-based front-runner and backup recommendation.
- A rate card is not automatically a formal quote or a shortlisted provider. Do not re-request Flexport's already received rate card.

**Important freshness caveat:** The canonical count above is dated 2026-11-21. The 2026-11-26 daily progress record describes later provider documents and clarification activity, including a Suaid quote/rate-card discrepancy against the canonical count. Reconcile the latest tracker, provider documents, and correspondence before repeating counts or changing canonical status. Do not resolve the discrepancy from an AI summary alone.

## Other material open context in the latest progress record

As recorded in `wins/daily-progress.md` through 2026-11-26; recheck live sources before acting:

- **TikTok Shop product-page access:** Seller Center listing management is accessible, but normal customer-facing product-page access remains unavailable. TikTok Support had not provided a fix; VPN use was recorded as a workaround for checks. Root cause is unconfirmed. Related Asana task: [1220386630404155](https://app.asana.com/1/1211857003594679/project/1213836032340905/task/1220386630404155).
- **Compact Food Mill replenishment:** A 1,000-unit / 125-case AWD-to-FBA replenishment was created and split by Amazon into 10 shipments. Last recorded state was Executing/Processing; delivery and FC receipt were not confirmed in that update.
- **CRAI Customer Insights:** The Asana task and report documentation were closed out on 2026-11-26. The historical action plan and case timeline are documented under `issues/customer-insights-report/`; do not imply a new Amazon resolution occurred on Nov 26.
- **R6 logistics optimization:** Broader route modeling and related work remain behind the temporary standard 3PL pricing focus unless management reprioritizes them.

These are dated context notes, not guaranteed live states.

## Reporting and documentation

- Weekly operations reporting is expected Mondays at 9:00 a.m. Eastern Time under the engagement agreement.
- `wins/daily-progress.md` is the primary daily progress log (newest entries first).
- `wins/notable-wins.md` holds verified notable outcomes.
- `todo/to-do.md` is Wesley's curated direction-setting and canonical priority/status record.
- `todo/` is Grok's audit workspace; Grok's reports are observational and do not change operational priorities.
- Project folders hold detailed project records, calculations, assumptions, and supporting documents.

Keep updates concise, dated, linked to evidence, and honest about what changed. A task closure or document update is not proof that the underlying business outcome was achieved.

## Retrieval guidance for WesAI

- Use this file only as fallback orientation when HA context is relevant and not already present.
- Do not inject the entire file into every prompt by default. Retrieve the relevant section or linked document when needed.
- Before answering a current-status question, inspect the relevant live tracker, Asana task, marketplace portal, source email, or project file.
- Start with `todo/to-do.md` for current priorities and canonical 3PL status; then check newer daily progress and supporting evidence for changes or discrepancies.
- Use `wins/daily-progress.md` for dated activity, not as a replacement for live system status.
- Use the relevant project folder for detailed R6, listing, inventory, shipment, or case context.
- If a source is inaccessible or a status cannot be verified, state that limitation.
- This file is a manually maintained context reference, not a live or automatically synchronized feed.

## Key references

- [HA-Operations README / command center](README.md)
- [AI Rules](ai-rules.md)
- [Canonical priorities and 3PL status](todo/to-do.md)
- [Daily progress log](wins/daily-progress.md)
- [Notable wins](wins/notable-wins.md)
- [R6 Logistics Optimization](projects/R6-logistics-optimization/)
