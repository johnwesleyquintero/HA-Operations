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
- **AGL baseline blocker:** Searched company email and Amazon AWD shipment records but could not locate an AGL freight quote or itemized freight-cost breakdown. A historical Bill of Lading (B/L **AMZDCN26JJJKW2GY**) and CBP Form 7501 were found for the same shipment, with matching B/L reference; these help identify the shipment but do not provide a usable ocean-freight charge or independently confirm that AGL arranged the freight. Do not estimate or enter a made-up AGL cost as the baseline.
- **HA Shipping Tracker access limitation:** The PO tab in **HA Shipping Tracker — “PURCHASE ORDERS · ONE ROW PER PO, FROM PI TO ARRIVAL”** lists document/payment checklist fields such as **BOL received, Entry summary, Shipping final bill, Balance 1 paid, and Balance 2 paid**. However, we do not currently have access to the underlying documents and payment records from that PO tab. The tracker entries alone do not provide the actual AGL freight quote, invoice, or payment amounts needed to establish a verified baseline.
- **Dependency / escalation needed:** Ask Justin or the person who manages freight bookings/payments where AGL booking confirmations, invoices, billing exports, and payment records are stored, or request access/copies for the identified historical shipment. Use the B/L references to match records: master B/L **YMJAW226837921**, house B/L **AMZDCN26JJJKW2GY**. Customs duties/taxes from Form 7501 must remain separate from ocean freight.

**Next actions**
1. Request access to the relevant HA Shipping Tracker PO supporting documents/payment records, and ask Justin or the freight-booking/accounts-payable owner for the historical AGL booking confirmation, freight invoice, billing export, or itemized shipment-cost record; identify the shipment using the B/L references above.
2. Obtain the exact AWD destination and missing supplier carton specifications.
3. Follow up with FCLGO on October 27 if a substantive quote/documentation response has not arrived.
4. Review Flexport's quoted charges and service scope against the AGL route.
5. Validate the workbook with one real shipment and two comparable paths; keep estimates and unknowns clearly labeled.

**Milestone watch**
- **October 31:** Multi-forwarder quoting process live and in use. Timing remains at risk while comparable quotes, verified inputs, access to historical supporting records, and the AGL baseline are outstanding.
- **November 30:** Total cost of ownership analysis and written recommendation delivered to Justin.
- **December 31:** At least one shipment completed under the new quoting process, with documented cost comparison.

### Update Log

| Date | Update | Blocker / Risk | Next Action |
|---|---|---|---|
| Oct 23, 2026 | Initial alternative-forwarder outreach and Flexport discovery have started; Tactical acknowledged the RFQ. | Current response status and quote coverage across all three markets need verification. | Review existing correspondence, follow up with current contacts, and secure comparable quotes. |
| Oct 24, 2026 | Completed the shipment comparison workbook audit and documented the information needed from forwarders/3PLs to compare quotes consistently, including quote terms, itemized costs, transit/delivery, customs, insurance, and service inclusions/exclusions. | Comparable quotes still need to be collected and validated across the relevant routes. | Use the audit checklist to request complete, itemized quotes and populate the comparison workbook with verified inputs. |
| Oct 25, 2026 | Expanded the investigation with a review of the actual workbook: identified unverified/missing cost inputs, sample-like shipment allocations, and a DDP double-counting/omission risk. Documented the validation approach: start with one real shipment and compare AGL against one alternative. | FCLGO has only acknowledged the two-container Classic + Compact RFQ; its itemized quote and documentation clarification are pending. Exact AWD destination, carton specifications, and a verified AGL cost breakdown are also outstanding. | Follow up with FCLGO on Oct 27 if needed; obtain missing shipment inputs; review Flexport scope; locate AGL costs; validate one real shipment before making a routing recommendation. |
| Oct 25, 2026 | Searched company email and Amazon AWD shipment records for the AGL baseline. Found a historical B/L and matching customs entry, but neither contains a usable ocean-freight cost breakdown or independently confirms AGL as the freight arranger. Reviewed the HA Shipping Tracker PO-tab fields, which list document/payment checklist items but do not give us access to the underlying documents or payment records. | **AGL baseline is blocked by both missing historical booking/invoice data and lack of access to the supporting PO documents/payment records.** Do not substitute customs duties/taxes or an unsupported estimate for ocean freight. | Request access/copies of the PO supporting documents and payment records; ask Justin or the freight-booking/AP owner for the AGL booking confirmation, freight invoice, billing export, or itemized shipment-cost record. Match using master B/L YMJAW226837921 and house B/L AMZDCN26JJJKW2GY. |

**Update rule:** Record confirmed progress, meaningful decisions, blockers, and next actions. Keep completed work distinct from planned work; revise status when evidence changes.
