# Hungry Artisan Daily Operations Audit — 2026-11-20

**Auditor:** Grok (independent review)  
**Date:** 20 November 2026  
**Scope:** Recent Gmail (Justin Hopkins, Wesley Quintero, suppliers/3PLs), Google Drive (meeting notes, dashboards), HA-Operations repository (to-do.md, R6 files, 3PL pricing records).  
**Authority note:** This is an observational audit and recommendation record only. It does not change priorities, mark work complete, or authorize external action.

## Executive Summary

- **Overall operational picture:** Temporary management direction (explicitly recorded in `to-do.md` as of 2026-11-20 and consistent with the 19 Nov Operations Team Meeting notes) has narrowed focus exclusively to collecting standard, itemized 3PL warehouse rate sheets. Broader freight-forwarder and multi-route logistics work remains deferred.
- **Most important development:** Progress on the sole active priority. California FBA Prep Center replied 19 Nov with an attached rate sheet; Prep Center LA sent a rate card the same day (forwarded to Justin); 3PL Guys sheet was already received and transcribed earlier (14 Nov). Several additional outreach emails went out on 19–20 Nov.
- **Biggest risk or missed commitment:** Limited number of formal, comparable rate sheets still in hand. Meeting notes indicate Justin expects results presented at the next meeting; continued delays in responses or incomplete documentation risk repeating the earlier multi-month lag noted in the meeting.
- **Immediate recommended focus:** Document and normalize the rate sheets already received (starting with California FBA Prep Center and Prep Center LA), send concise daily follow-ups on outstanding requests, and prepare a simple side-by-side comparison for the next management review. Do not expand into freight-forwarder work.

## Priority Action Items

| Priority | Action | Owner | Due / Timing | Status | Next Step |
|----------|--------|-------|--------------|--------|-----------|
| Critical | Compile and normalize received standard 3PL rate sheets (3PL Guys, California FBA Prep Center, Prep Center LA) into a simple comparison | Wesley | Next meeting (target before end of week / early next week) | In progress — sheets received, not yet centralized | Extract key fees (receiving, storage, pick/pack, monthly minimums, setup) from attachments and document in a single working file; label assumptions and gaps |
| High | Follow up on pending 3PL rate-sheet requests (Matrix Fulfillment, Tactical Logistics / Ryan Cao, and any contact-form submissions) | Wesley | Daily, short emails | Open — multiple requests sent 19–20 Nov | Send one-sentence follow-ups; copy Justin where appropriate; track response status |
| High | Confirm Flexport 3PL capability details and request standard rate sheet | Wesley | This week | Partial — Jordan confirmed capability 18 Nov; no rate sheet yet | Reply requesting itemized standard rates for receiving/storage/fulfillment |
| Medium | Document California FBA Prep Center rate sheet (attachment received 19 Nov) and note their request for volume data | Wesley | Immediate | Received | Save/transcribe key rates; prepare answers to their volume questions if needed for a formal proposal |
| Low | Routine inventory and marketplace monitoring (canning kit levels, AWD in-transit, TikTok regional access) | Wesley | Ongoing | Monitoring | Escalate only if urgent operational impact; otherwise defer per current priority |

## Recent Progress

- **19–20 Nov 2026:** Multiple standard 3PL rate-sheet requests sent by Wesley to California FBA Prep Center, Prep Center LA, and Matrix Fulfillment.
- **19 Nov:** California FBA Prep Center replied with attached rate sheet (`SHF_Price_072026.pdf`) and offered a call; Wesley forwarded Prep Center LA rate card to Justin.
- **14 Nov (previously documented):** 3PL Guys rate sheet received and transcribed in `projects/3pl-guys-pricing.md`.
- **18 Nov:** Flexport (Jordan Politi) confirmed ability to provide 3PL services; email forwarded to Justin 20 Nov.
- Meeting notes (Gemini, Operations Team Meeting 19 Nov) record Justin’s clarification to focus strictly on 3PL warehouses rather than freight companies.

Evidence: Gmail threads (subjects “Request for Standard 3PL Rate Sheet”, Flexport thread, Prep Center LA); `projects/3pl-guys-pricing.md`; Drive Gemini notes document.

## Outstanding Follow-ups

- Tactical Logistics (Ryan Cao) — follow-up sent 19 Nov on 3PL rate sheet; no reply yet in reviewed threads.
- Matrix Fulfillment — request sent 20 Nov; pending.
- Rivera Air Freight — older request for pricing sheet (14 Nov); not active under current 3PL-only focus.
- Suaid Global — earlier ocean/3PL discussion; deferred.
- California FBA Prep Center — rate sheet received; they asked for first-shipment volume, monthly order split, and service mix to prepare a proposal.
- Prep Center LA — rate card received; status of any further clarification needed.
- Flexport 3PL rates — capability confirmed; formal sheet not yet requested/received.

## Decisions and Changes

- **Temporary exclusive focus on standard 3PL pricing** (recorded in root `to-do.md` dated 2026-11-20 and aligned with 19 Nov meeting notes). Broader logistics optimization, freight-forwarder comparisons, Forest Leopard evaluation, and most listing/creative items are explicitly deferred until the next management meeting or explicit reprioritization.
- Justin directed direct outreach to 3PL warehouses (not via third parties or friends) and concise follow-ups.
- Spreadsheet creation paused in favor of gathering raw rate sheets.

Source: `to-do.md` Temporary Execution Focus section; Gemini meeting notes (Drive + email).

## Risks and Blockers

- **Rate-sheet coverage still thin:** Only a small number of formal sheets in hand after prior delays noted in the meeting. Risk of insufficient comparison data for the next review.
- **Inventory in transit:** Multiple AWD inbound shipments remain in transit (per dashboards and meeting notes), limiting new shipment creation under current 60-day constraints. Canning kit levels described as low and requiring monitoring.
- **TikTok regional access issues:** Support cases pending technical routing (noted in meeting); currently deferred under 3PL priority.
- **Documentation lag:** Received rate sheets (especially California FBA Prep and Prep Center LA) are not yet transcribed or compared in the repository, creating a visibility gap.
- AI-generated meeting notes are useful context but not authoritative; primary evidence is the emails and `to-do.md`.

## Deferred and Completed Items

**Deferred (per `to-do.md` and meeting direction):**
- Broader multi-forwarder / R6 logistics optimization beyond standard 3PL rates.
- Forest Leopard China-based logistics evaluation.
- Main-image CTR tracking and creative text changes.
- Compact listing A/B test decision.
- Most listing and promotional experiments.

**Completed / resolved for current focus:**
- 3PL Guys rate sheet received and documented (14 Nov).
- Initial round of direct 3PL outreach emails sent (19–20 Nov).

No prior audit reports exist in `todo/` to compare against.

## Sources Reviewed

- **Gmail:** Threads involving Wesley Quintero and Justin Hopkins on 3PL rate sheets (19–20 Nov), Flexport (Jordan Politi, updated 18 Nov), California FBA Prep Center (19 Nov reply with attachment), Prep Center LA, Tactical Logistics, and others. Meeting notes email from Gemini (19 Nov).
- **Google Drive:** HA Ops Dashboards spreadsheet (recent inventory/account health views); Operations - Team Meeting notes document (Gemini, 19 Nov 2026).
- **GitHub (johnwesleyquintero/HA-Operations):** `to-do.md` (Temporary Execution Focus), `projects/3pl-guys-pricing.md`, `projects/R6-update-log.md`, `projects/R6-logistics-optimization.md`, `todo/README.md`, repository tree.

## Recommended Next Steps

1. Transcribe or extract the key line items from the California FBA Prep Center rate-sheet attachment and the Prep Center LA rate card into a simple comparison table (alongside the existing 3PL Guys transcription). Label any missing or unclear fees.
2. Send short, one-sentence follow-ups today on any 3PL requests older than 24–48 hours (Tactical, Matrix, etc.).
3. Request a standard rate sheet from Flexport for their 3PL services.
4. Prepare a one-page summary of received rates and outstanding gaps for the next meeting with Justin.
5. Continue daily email checks focused on 3PL responses; escalate only true operational blockers outside this priority.

**Assumptions labeled:** Meeting notes are treated as useful context consistent with written priorities in `to-do.md`, not as independent proof of decisions. Rate-sheet attachments were noted from email metadata and previews; full contents should be verified by Wesley before comparison use.

---
*End of audit. Next dated report should highlight changes since this one.*
