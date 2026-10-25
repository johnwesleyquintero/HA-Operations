# R6 Logistics Optimization — Progress Update Log

> **Purpose:** Track actual progress, blockers, decisions, and next actions toward the R6 milestones. Update this section as meaningful work happens.

### Current Status — October 24, 2026

**Overall status:** In progress — October milestone at risk until outreach and quote status are confirmed.

**Progress so far**
- Initial outreach to alternative freight forwarders has started.
- Tactical acknowledged the RFQ and routed it to Ryan.
- An initial discovery conversation with Flexport has taken place.
- The existing logistics strategy and RFQ work provide a starting point for comparing alternatives against AGL.
- Completed the Shipment Logistics Comparison workbook audit and identified the quote details and cost inputs to request from freight forwarders and 3PLs, including Incoterms, rate breakdowns, transit times, destination delivery, customs/insurance, and included services or exclusions.

**Outstanding**
- Confirm the latest response and follow-up status for each forwarder, including AGL.
- Obtain usable, comparable quotes for the relevant China-to-US, China-to-CA, and China-to-UK routes.
- Confirm the quote comparison framework is usable with actual shipment data.
- Quantify Amazon ecosystem benefits and costs before recommending any routing changes.

**Next actions**
1. Review existing forwarder correspondence and the current tracker; identify only the follow-ups needed.
2. Follow up with existing contacts and secure the first comparable quote.
3. Continue collecting comparable rates for the three markets.
4. Update this log when a material milestone is achieved or a blocker requires a decision.

**Milestone watch**
- **October 31:** Multi-forwarder quoting system live and in use.
- **November 30:** Total cost of ownership analysis and written recommendation delivered to Justin.
- **December 31:** At least one shipment completed under the new quoting process, with documented cost comparison.

### Current Status — October 25, 2026

**Overall status:** In progress — investigation has clarified the workbook's readiness gaps and the active FCLGO RFQ, but comparable verified quotes are still pending.

**Investigation findings**
- Audited the actual `HA Shipment Logistics Comparison (DRAFT).xlsx` workbook. It is a useful cost-comparison framework, but it is not yet validated enough to support a real routing decision without verified shipment inputs and a shipment-level calculation check.
- The `Shipment Setup` tab contains sample-like allocations for 1,000 Classic Food Mill units (500 AWD, 250 FBA Direct, 100 Walmart WFS, 150 TikTok FBT). These are not confirmed shipment instructions and must be cleared or replaced before real use.
- Key inputs remain incomplete or unverified, including carton dimensions/CBM, gross carton weight, unit COGS, duty/HTS assumptions, and rate-card values/dates. A zero output where inputs are missing must not be interpreted as zero cost.
- Validate the scope of any DDP quote before combining it with other charges, to avoid double-counting costs that are already included or omitting excluded charges.
- The recommended validation path is deliberately small: use one real shipment and compare AGL with one alternative before expanding the analysis to more scenarios.

**Active RFQ — FCLGO**
- Requested pricing for **two 40' HQ containers** from China via Yantian to Los Angeles, with final delivery to Amazon AWD (exact AWD facility address still needed).
- Scope currently includes **Classic Food Mill: 5,808 units at $7.48** and **Compact Food Mill: 6,000 units at $7.12** — **11,808 units** and **$86,163.84 total product value**. Premium is not part of this RFQ.
- Requested itemized ocean freight, origin/destination charges, customs clearance, duties, AWD final-mile delivery, and transit time.
- On October 24, FCLGO acknowledged the request and said they would reply. This is an acknowledgment only; no substantive itemized quote has been received yet.
- FCLGO asked about FDA documentation/import filing for stainless-steel food-contact kitchen tools. Supplier/broker confirmation is pending; do not assume the required documentation is available or make a compliance claim without confirmation.
- **Next follow-up:** If no substantive response arrives, follow up on October 27.

**Other quote coverage**
- Flexport has provided initial quote information for one 40' and two 40' containers from Jieyang, Guangdong, to Southern California. Review inclusions, exclusions, route, transit, and AWD final delivery before treating it as comparable to AGL.
- Tactical acknowledged the initial RFQ and routed it to Ryan; a quote is not yet confirmed in this log.
- The current AGL quote/cost breakdown still needs to be located and verified from booking details, email, Seller Central, tracker records, or prior confirmations/invoices.

**Next actions**
1. Obtain the exact AWD destination and missing supplier carton specifications.
2. Follow up with FCLGO on October 27 if a substantive quote/documentation response has not arrived.
3. Review Flexport's quoted charges and service scope against the AGL route.
4. Locate the source AGL cost breakdown and capture its quote reference, validity, route, container, charges, delivery scope, and transit time.
5. Validate the workbook with one real shipment and two comparable paths; keep estimates and unknowns clearly labeled.

**Milestone watch**
- **October 31:** Multi-forwarder quoting process live and in use. Timing remains at risk while comparable quotes and verified inputs are outstanding.
- **November 30:** Total cost of ownership analysis and written recommendation delivered to Justin.
- **December 31:** At least one shipment completed under the new quoting process, with documented cost comparison.

### Update Log

| Date | Update | Blocker / Risk | Next Action |
|---|---|---|---|
| Oct 23, 2026 | Initial alternative-forwarder outreach and Flexport discovery have started; Tactical acknowledged the RFQ. | Current response status and quote coverage across all three markets need verification. | Review existing correspondence, follow up with current contacts, and secure comparable quotes. |
| Oct 24, 2026 | Completed the shipment comparison workbook audit and documented the information needed from forwarders/3PLs to compare quotes consistently, including quote terms, itemized costs, transit/delivery, customs, insurance, and service inclusions/exclusions. | Comparable quotes still need to be collected and validated across the relevant routes. | Use the audit checklist to request complete, itemized quotes and populate the comparison workbook with verified inputs. |
| Oct 25, 2026 | Expanded the investigation with a review of the actual workbook: identified unverified/missing cost inputs, sample-like shipment allocations, and a DDP double-counting/omission risk. Documented the validation approach: start with one real shipment and compare AGL against one alternative. | FCLGO has only acknowledged the two-container Classic + Compact RFQ; its itemized quote and documentation clarification are pending. Exact AWD destination, carton specifications, and a verified AGL cost breakdown are also outstanding. | Follow up with FCLGO on Oct 27 if needed; obtain missing shipment inputs; review Flexport scope; locate AGL costs; validate one real shipment before making a routing recommendation. |

**Update rule:** Record confirmed progress, meaningful decisions, blockers, and next actions. Keep completed work distinct from planned work; revise status when evidence changes.
