# Walmart WFS Phantom Inbound — Shipment 8862220WFA

**Internal status:** Closed — reporting control in place; Walmart-side record remains unresolved  
**Last reviewed:** November 18, 2026  
**Owner:** Wesley Quintero  
**Walmart case:** [#16866157](https://seller.walmart.com/supporthub/your-cases/case-details?caseNumber=16866157) — Seller Support closed the case and stated the shipment can no longer be canceled by Walmart.  
**Asana:** [Resolve Walmart WFS Phantom Inbound Shipment 8862220WFA](https://app.asana.com/1/1211857003594679/project/1213836032340905/task/1220010725209075)

## Issue and disposition

An accidentally created WFS shipping plan remains in Seller Center as an expected inbound shipment even though HA did not intend to ship the inventory. Seller Center blocks cancellation/deletion. Walmart's November 11 response reiterated that it cannot cancel the shipment from its end, directed HA to contact the assigned carrier, and marked support case #16866157 closed.

HA's prior clarification remains: no physical shipment was intended or sent, and HA does not use FedEx for this shipment. Walmart's Seller Center record nevertheless shows WFS-FEDEX and a FedEx tracking number. Further carrier/Walmart escalation is being discontinued as an internal operational decision. This does **not** mean Walmart corrected or removed the record.

- **Shipping Plan ID:** HUN-1781878717671
- **Shipment ID:** 8862220WFA
- **Destination:** IND3, 5756 Enterprise Dr, McCordsville, IN 46055
- **Ship-from shown:** 16155 W Elwood St, Goodyear, AZ 85338
- **Carrier shown in Walmart Seller Center:** WFS-FEDEX
- **Created:** June 19, 2026
- **Estimated delivery:** June 26, 2026
- **Units shown shipped:** 918
- **Units received:** 0
- **Seller Center status:** Awaiting transit
- **Physical shipment:** None intended or sent; the plan was created accidentally by a previous team member.

## Reporting control

Wesley has added a formula to the reporting sheet to exclude this specific phantom shipment and a validation check to prevent its 918 units from being included in reporting.

**Control boundary:** This is an internal reporting safeguard. It does not modify Walmart Seller Center, cancel the shipment, or remove Walmart's underlying inbound record.

**Ongoing validation**
- Confirm shipment 8862220WFA / plan HUN-1781878717671 remains excluded from the relevant inbound/reporting output.
- Confirm the 918 phantom units do not inflate reported inbound inventory or replenishment calculations.
- Keep actual physical inventory and valid inbound shipments included normally; do not apply a broad exclusion to other WFS shipments.
- If the formula or source structure changes, retest the exclusion and its validation check before publishing the report.
- Reopen the issue only if the phantom shipment leaks into reporting, affects a replenishment decision, or Walmart provides a new actionable path.

The formula has been reported as added by Wesley; this record does not claim an independent test result or Walmart-side correction.

## Support history

- **Oct 29–Nov 9:** Case #16866157 was submitted, escalated, and followed up. Walmart ultimately said the shipment was Awaiting Transit with an active carrier and shipping quote and directed HA to contact FedEx.
- **Nov 9:** HA clarified it uses ESTES, not FedEx, and requested verification of Walmart's carrier assignment. FedEx tracking #528067050994 showed shipment information sent only, with no pickup scan visible at the time.
- **Nov 11:** Walmart Seller Support stated the shipment could no longer be canceled from Walmart's end, directed HA to contact the assigned carrier partner, and confirmed the case was closed after leadership review.
- **Nov 18:** HA disposition: stop pursuing the support/carrier escalation; rely on the spreadsheet exclusion and validation control to keep the phantom 918 units out of reporting. Retain this case record for audit traceability.

## Closure decision

**Closed internally — reporting protected by an explicit shipment-level exclusion and validation check.**

- Walmart support case: Closed by Walmart.
- Walmart Seller Center record: Still present; no backend correction confirmed.
- Physical shipment: None intended or sent.
- Reporting: Formula and validation check added by Wesley; continue routine validation.
- Further Walmart/FedEx follow-up: Not planned unless the reporting control fails or a new material operational impact appears.

## Related records

- [Walmart case #16866157](https://seller.walmart.com/supporthub/your-cases/case-details?caseNumber=16866157)
- [WFS shipping plan HUN-1781878717671](https://seller.walmart.com/wfs/shipments/order-details/HUN-1781878717671)
- [Asana task](https://app.asana.com/1/1211857003594679/project/1213836032340905/task/1220010725209075)
