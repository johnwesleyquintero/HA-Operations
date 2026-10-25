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
- Flexport provided an itemized quote for two 40' HQ containers from Shenzhen/Yantian to Los Angeles (Quote ID **Quote-5822794**, Shipment ID **FLEX-4278038**). The quoted total is **$17,022.13**, but the quote expired on **October 15, 2026** and needs to be refreshed before booking. It is FOB, customs brokerage is declined, and the quote does not confirm final-mile delivery to the AWD facility. See the preliminary comparison section below; do not treat the headline difference as verified savings/cost until scopes are normalized.
- Tactical acknowledged the initial RFQ and routed it to Ryan; a quote is not yet confirmed in this log.
- **AGL baseline blocker:** Searched company email and Amazon AWD shipment records but could not locate an AGL freight quote or itemized freight-cost breakdown. A historical Bill of Lading (B/L **AMZDCN26JJJKW2GY**) and CBP Form 7501 were found for the same shipment, with matching B/L reference; these help identify the shipment but do not provide a usable ocean-freight charge or independently confirm that AGL arranged the freight. Do not estimate or enter a made-up AGL cost as the baseline.
- **HA Shipping Tracker access limitation:** The PO tab in **HA Shipping Tracker — “PURCHASE ORDERS · ONE ROW PER PO, FROM PI TO ARRIVAL”** lists document/payment checklist fields such as **BOL received, Entry summary, Shipping final bill, Balance 1 paid, and Balance 2 paid**. However, we do not currently have access to the underlying documents and payment records from that PO tab. The tracker entries alone do not provide the actual AGL freight quote, invoice, or payment amounts needed to establish a verified baseline.
- **Dependency / escalation needed:** Ask Justin or the person who manages freight bookings/payments where AGL booking confirmations, invoices, billing exports, and payment records are stored, or request access/copies for the identified historical shipment. Use the B/L references to match records: master B/L **YMJAW226837921**, house B/L **AMZDCN26JJJKW2GY**. Customs duties/taxes from Form 7501 must remain separate from ocean freight.

### Preliminary Cost Comparison — Amazon AWD Estimate vs. Flexport Quote (October 25, 2026)

**Purpose:** Record the evidence currently available before entering assumptions into the draft comparison workbook. This is a preliminary reference comparison, not a validated total-landed-cost analysis.

| Field | Amazon AWD shipment record | Flexport quote |
|---|---|---|
| Record / reference | AWD Shipment ID **STAR-W3SYTEYFUNY3K**; Workflow ID **wfcfe56fcb-05ca-454b-836e-4ea2a5ef1f51** | Shipment ID **FLEX-4278038**; Quote ID **Quote-5822794** |
| Displayed total | **$14,395.67 estimated shipping fees** | **$17,022.13 quoted total** |
| Status / date | Shipment workflow created July 6, 2026; total is explicitly an estimate | Pending approval; quote expiration shown as October 15, 2026 — refresh required |
| Cargo / equipment | 1,966 boxes; 11,796 units; 1 SKU | 2 × 40' HQ containers; total weight and volume are not populated in the quote text |
| Route shown | Ship-from Jieyang, Guangdong; origin city Yantian; delivery to IUTE, 16155 W Elwood St, Goodyear, AZ 85338 | Pickup Shenzhen; departure port Yantian; arrival port Los Angeles, CA; final AWD delivery is not shown |
| Service / terms | Amazon AWD shipping workflow; detailed service inclusions not established by the displayed total | Ocean FCL; **FOB**; U.S. customs brokerage **declined**; insurance and carbon offset included |
| Transit estimate | Not shown in the record provided | Likely 25 days; latest estimate 33 days; carrier estimate 22–29 days |
| Itemization | No itemized breakdown in the screenshot provided | FCL 2 × $8,350 = $16,700; AMS $35; ISPS $30; booking $85; document turnover $65; import handling $75; carbon offset $32.13; total $17,022.13 |

**Arithmetic comparison (headline figures only)**

- Flexport quoted total minus Amazon AWD estimated fees: **$17,022.13 − $14,395.67 = $2,626.46**.
- This is an apparent **18.24% higher** Flexport figure relative to the Amazon estimate.
- These figures are **not yet apples-to-apples**. Amazon's number is an estimate with unverified inclusions/final amount; Flexport's quote has customs brokerage declined and does not confirm delivery to the final AWD facility. Do not report the $2,626.46 as verified extra cost or a final savings comparison.

**Scope and data gaps to resolve before any conclusion**

1. Obtain the final Amazon/AGL bill or invoice and confirm what the **$14,395.67** estimate includes, including whether it covers final AWD delivery and which origin/destination charges are included.
2. Refresh Flexport's expired quote and request a comparable all-in scope through the exact AWD facility, with U.S. customs brokerage, duties/taxes, destination charges, trucking/final-mile delivery, and exclusions explicitly itemized.
3. Confirm that both records represent the same cargo and service scope. The AWD screenshot shows **11,796 units**, while the current RFQ notes show **11,808 units** (Classic FM 5,808 + Compact FM 6,000); reconcile the 12-unit discrepancy and confirm carton/weight/CBM data.
4. Confirm the Amazon shipment's actual freight arranger before labeling the AWD estimate an **AGL** cost. The AWD workflow alone does not prove AGL arranged the shipment.
5. Only calculate normalized cost differences after aligning cargo, equipment, route, final destination, inclusions, exclusions, and quote validity.

**Current assessment:** Useful initial evidence exists for both options, but the historical AGL/actual Amazon final cost and comparable Flexport service scope remain unverified. The workbook should not be used to turn missing inputs into zero-cost assumptions. Continue collecting and documenting quote inputs, but defer any final price recommendation until the gaps above are resolved.

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

### Flexport Quote Detail and Workbook Readiness — October 25, 2026

Created [`projects/flexport.md`](https://github.com/johnwesleyquintero/HA-Operations/blob/main/projects/flexport.md) to preserve the Flexport quote's itemized charges, terms, expiration, known workbook fields, unresolved inputs, and validation steps.

- **Workbook readiness:** Partial. The known quote fields and $17,022.13 itemized total can be entered, with the quote clearly marked expired / refresh required.
- **Not decision-ready:** Customs brokerage is declined; final AWD delivery is unconfirmed; weight/CBM are missing; cargo quantity differs by 12 units between the Amazon record and current RFQ notes; and the Amazon figure remains an estimate rather than a verified AGL final cost.
- **Data-handling rule:** Leave unknown costs pending rather than entering zero. Do not treat the $2,626.46 headline difference as verified savings or extra cost.
- **Next action:** Refresh Flexport's quote and normalize service scope and cargo details against a verified Amazon/AGL final invoice before making a routing recommendation.

### AGL Baseline and Workbook Readiness — October 25, 2026

Created [`projects/agl.md`](https://github.com/johnwesleyquintero/HA-Operations/blob/main/projects/agl.md) to consolidate the historical Amazon AWD shipment evidence, the missing AGL source records, and the end-to-end workbook readiness checklist.

- **Evidence located:** AWD shipment `STAR-W3SYTEYFUNY3K`, estimated shipping fee $14,395.67, house B/L `AMZDCN26JJJKW2GY`, master B/L `YMJAW226837921`, and broker file `INL-12791577`.
- **Baseline still blocked:** The current evidence does not establish AGL as the booking party or provide the final itemized freight invoice. The CBP Form 7501 amount is duties/taxes/fees, not ocean freight.
- **Workbook readiness inputs:** Confirm cargo/PO identity, reconcile 11,796 vs. 11,808 units, obtain carton dimensions/weight/CBM and exact AWD destination, source AGL final charges and payment detail, refresh Flexport, price customs brokerage/final-mile delivery, verify duties/HTS and rate-card assumptions, and replace sample-like Shipment Setup allocations.
- **Guardrail:** Keep unknowns Pending rather than zero and do not treat the $2,626.46 headline gap as a validated comparison.

### Update Log

| Date | Update | Blocker / Risk | Next Action |
|---|---|---|---|
| Oct 23, 2026 | Initial alternative-forwarder outreach and Flexport discovery have started; Tactical acknowledged the RFQ. | Current response status and quote coverage across all three markets need verification. | Review existing correspondence, follow up with current contacts, and secure comparable quotes. |
| Oct 24, 2026 | Completed the shipment comparison workbook audit and documented the information needed from forwarders/3PLs to compare quotes consistently, including quote terms, itemized costs, transit/delivery, customs, insurance, and service inclusions/exclusions. | Comparable quotes still need to be collected and validated across the relevant routes. | Use the audit checklist to request complete, itemized quotes and populate the comparison workbook with verified inputs. |
| Oct 25, 2026 | Expanded the investigation with a review of the actual workbook: identified unverified/missing cost inputs, sample-like shipment allocations, and a DDP double-counting/omission risk. Documented the validation approach: start with one real shipment and compare AGL against one alternative. | FCLGO has only acknowledged the two-container Classic + Compact RFQ; its itemized quote and documentation clarification are pending. Exact AWD destination, carton specifications, and a verified AGL cost breakdown are also outstanding. | Follow up with FCLGO on Oct 27 if needed; obtain missing shipment inputs; review Flexport scope; locate AGL costs; validate one real shipment before making a routing recommendation. |
| Oct 25, 2026 | Searched company email and Amazon AWD shipment records for the AGL baseline. Found a historical B/L and matching customs entry, but neither contains a usable ocean-freight cost breakdown or independently confirms AGL as the freight arranger. Reviewed the HA Shipping Tracker PO-tab fields, which list document/payment checklist items but do not give us access to the underlying documents or payment records. | **AGL baseline is blocked by both missing historical booking/invoice data and lack of access to the supporting PO documents/payment records.** Do not substitute customs duties/taxes or an unsupported estimate for ocean freight. | Request access/copies of the PO supporting documents and payment records; ask Justin or the freight-booking/AP owner for the AGL booking confirmation, freight invoice, billing export, or itemized shipment-cost record. Match using master B/L YMJAW226837921 and house B/L AMZDCN26JJJKW2GY. |
| Oct 25, 2026 | Added a preliminary comparison of Amazon AWD's $14,395.67 estimated shipping fees and Flexport's $17,022.13 itemized quote. Calculated a $2,626.46 / 18.24% headline difference and documented why it is not yet a valid like-for-like conclusion. | Amazon figure is an estimate with unverified inclusions/final cost; Flexport quote expired Oct 15, customs brokerage is declined, and final AWD delivery is not confirmed. Cargo quantity also differs by 12 units between the AWD record (11,796) and RFQ notes (11,808). | Refresh Flexport quote, verify the Amazon final bill and service inclusions/AGL booking identity, confirm final AWD delivery scope, and reconcile shipment quantities before making a cost recommendation. |

| Oct 25, 2026 | Documented Flexport's quote and workbook readiness in `projects/flexport.md`; confirmed known fields can be entered but the expired quote and scope/data gaps prevent a valid comparison. | Flexport quote expired Oct 15; customs brokerage declined; final AWD delivery, weight/CBM, quantity reconciliation, and verified Amazon/AGL final cost remain outstanding. | Refresh Flexport, confirm delivery/customs scope and cargo inputs, obtain the final Amazon/AGL invoice, then validate the workbook with normalized inputs. |

| Oct 25, 2026 | Added `projects/agl.md` with the AGL baseline evidence, records needed, and workbook readiness checklist. | Historical AGL booking party and final itemized cost remain unverified; shipment quantity, carton/weight/CBM, destination, and comparable service scope need confirmation. | Request AGL booking/invoice/billing and payment records using the B/L references; reconcile shipment data; refresh Flexport and complete workbook validation with verified inputs. |


| Oct 25, 2026 | Updated the root README's **Priority Work & Reports** R6 row to surface the workbook blocker, shipment-quantity reconciliation, required cargo specs, missing AGL source records, and links to the AGL/Flexport records. | Documentation and navigation are clearer, but the underlying shipment inputs, verified AGL final cost, and comparable current quote are still outstanding. | Use the README as the starting point; request AGL booking/invoice/payment records and missing shipment specs, refresh Flexport, and validate one real shipment before drawing cost conclusions. |

**Update rule:** Record confirmed progress, meaningful decisions, blockers, and next actions. Keep completed work distinct from planned work; revise status when evidence changes.


| Oct 25, 2026 | Added a 60-second executive summary to the top of `projects/R6-logistics-optimization.md`, covering current progress, verified vs. unverified costs, the key blocker, next actions, and milestone status for Victoria and Justin. | Comparable current quotes and a verified AGL final-cost baseline remain outstanding; no savings claim is supported yet. | Use the summary for leadership updates; prioritize AGL source records, reconcile shipment data, refresh comparable quotes, and validate one real shipment. |
