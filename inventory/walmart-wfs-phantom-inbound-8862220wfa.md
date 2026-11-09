# Walmart WFS Phantom Inbound — Shipment 8862220WFA

**Status:** Open — At Risk; carrier assignment discrepancy and Walmart backend correction unresolved  
**Last reviewed:** November 9, 2026  
**Owner:** Wesley Quintero  
**Walmart case:** [#16866157](https://seller.walmart.com/supporthub/your-cases/case-details?caseNumber=16866157)  
**Asana:** [Resolve Walmart WFS Phantom Inbound Shipment 8862220WFA](https://app.asana.com/1/1211857003594679/project/1213836032340905/task/1220010725209075)

## Issue

An accidentally created WFS shipping plan remains in Seller Center as an expected inbound shipment even though HA did not intend to ship the inventory. Seller Center blocks cancellation/deletion.

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

## Carrier discrepancy and tracking

Walmart's Nov 9 response stated that the shipment is in **Awaiting Transit** with an active carrier and shipping quote, so Walmart cannot cancel it directly at this stage. Support directed HA to contact the assigned carrier partner, FedEx, to cancel the shipment and void the movement.

HA clarified to Walmart that we use **ESTES, not FedEx**, and asked Walmart to verify why Seller Center shows WFS-FEDEX and a FedEx shipment record.

- **FedEx tracking number displayed:** 528067050994
- **Service shown:** FedEx Ground
- **Origin / destination:** Goodyear, AZ → McCordsville, IN
- **Tracking status observed:** “Shipment information sent to FedEx”; no physical pickup scan is visible.
- **Carrier action:** HA is attempting to contact FedEx through an official support channel to request cancellation/label void, confirmation whether the shipment was ever tendered, and clarification of any charges.
- **Confirmation:** No FedEx cancellation, label void, or carrier-side resolution has been confirmed.

The tracking status alone does not establish that FedEx physically received the shipment. Keep the distinction between label creation/electronic shipment information and physical carrier possession clear.

## Business impact

The phantom 918-unit inbound record may distort WFS inventory visibility, replenishment decisions, and forecast planning by making inventory appear to be on the way.

## Support history

- **Oct 29:** Case #16866157 submitted; Walmart acknowledged and escalated internally.
- **Oct 30:** Walmart advised an update was expected on or before Nov 8, 2026.
- **Nov 2:** Walmart reported feedback from an initial internal team and coordination with another specialized team.
- **Nov 3:** Walmart said the specialized team had not yet provided findings.
- **Nov 4:** Walmart again said no specialized-team update was available; case remained under review. Support said no seller action was required at that time.
- **Nov 5:** HA followed up requesting substantive findings, an explanation for the 918-unit shipped quantity despite no physical shipment, confirmation of backend correction status, and confirmation that the Nov 8 update commitment remained on track.
- **Nov 6 review:** No new Walmart response or correction had been confirmed.
- **Nov 9:** Walmart advised that the shipment is in Awaiting Transit with an active carrier and shipping quote, and directed HA to contact FedEx to cancel/void the shipment from the carrier side.
- **Nov 9:** HA clarified that it uses ESTES, not FedEx, and requested Walmart verify the WFS-FEDEX carrier assignment. HA is also attempting to contact FedEx using tracking #528067050994. Tracking showed electronic shipment information only, with no pickup scan. No carrier cancellation or Walmart backend correction has been confirmed.

## Requested resolution

1. Verify the actual carrier assignment for shipment 8862220WFA and explain why Walmart displays WFS-FEDEX when HA uses ESTES.
2. If FedEx is in fact assigned, cancel the shipment and void the label/movement; confirm whether it was tendered and whether charges were incurred.
3. Remove, cancel, or deactivate the incorrect shipping plan and associated inbound record through Walmart's backend.
4. Ensure the 918 units are no longer treated as expected inbound inventory.
5. Correct or refresh inventory reporting.
6. Confirm whether historical inventory or forecasting data needs to be refreshed.
7. Confirm whether any seller-side action is required after correction.

## Next steps

- Follow up with FedEx through an official support channel about tracking #528067050994; request cancellation, label void, tender/pickup confirmation, and charge status.
- Keep Walmart case #16866157 open. Ask Walmart to verify the WFS-FEDEX assignment against HA's use of ESTES and coordinate internally if the carrier record is incorrect.
- Continue requesting Walmart backend correction/deactivation of the phantom 918-unit inbound record; carrier contact alone does not resolve the inventory issue.
- After carrier status and Walmart correction are confirmed, verify that the 918 units no longer appear in WFS inbound inventory, inventory reports, or replenishment/forecast planning.
- Do not treat this as a physical shipment or create a duplicate shipment to compensate for the phantom record.

## Related records

- [Walmart case #16866157](https://seller.walmart.com/supporthub/your-cases/case-details?caseNumber=16866157)
- [WFS shipping plan HUN-1781878717671](https://seller.walmart.com/wfs/shipments/order-details/HUN-1781878717671)
- [Asana task](https://app.asana.com/1/1211857003594679/project/1213836032340905/task/1220010725209075)
