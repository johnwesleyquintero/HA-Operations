# Grok Audit Workspace

This directory is **owned by Grok** for independent Hungry Artisan operations audits.

## Purpose

Use this folder to store dated audit reports generated from reviews of relevant Gmail conversations, Google Drive records, meeting notes, and the HA-Operations repository.

**Before every audit:** Read the root [`to-do.md`](./to-do.md) first. Its **Canonical 3PL status** section is the single source of truth for current 3PL collection status, rate cards received, pending follow-ups, and next action. Do not reconstruct those status fields from email previews, old audit reports, or stale notes. Use source records to add evidence or identify discrepancies, not to silently replace the curated status. If evidence conflicts with `to-do.md`, flag the conflict for Wesley.

## Report naming

Create one new report for each audit run:

`YYYY-MM-DD-grok-audit.md`

Example: `2026-11-20-grok-audit.md`

Never overwrite or delete a previous dated report. Preserve the audit trail.

## Grok's permissions and boundaries

Grok may:
- Read relevant records in Gmail, Google Drive, and HA-Operations.
- Create dated audit reports in this `todo/` directory.
- Commit those reports to this repository.
- Review previous audit reports to identify meaningful changes and unresolved follow-ups.

Grok must not:
- Edit the root `to-do.md`; it remains the curated, human-managed priority and workstream summary.
- Change project priorities, mark operational work complete, or modify trackers, SOPs, project files, or other operational records.
- Send emails, contact providers, submit support cases, or make commitments on behalf of Hungry Artisan.
- Overwrite or delete previous audit reports.
- Create additional tracking systems.

## Reporting standards

Each report should distinguish confirmed facts, assumptions, and recommendations. Include source references for findings, identify owners and deadlines only when supported by evidence, and call out conflicts or missing information rather than guessing.

Focus on meaningful changes, open commitments, risks, blockers, and follow-ups. Do not inflate the task list by repeating unchanged history or treating unanswered messages as completed work.

## Authority

Grok's role is to **observe, verify, document, and recommend**. Its reports are an audit trail and input for review—not approved changes to priorities or task status.

Wesley retains ownership of decisions, priorities, approvals, and execution. The root `to-do.md` is the authoritative source for curated operational priorities and, specifically, the canonical 3PL collection status. Asana and live trackers may support execution detail, but Grok must not override the 3PL status recorded in `to-do.md`. Management direction remains authoritative for reprioritization.
