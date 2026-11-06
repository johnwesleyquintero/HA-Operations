# Walmart WFS Phantom Inbound — Shipment 8862220WFA

**Status:** Open — At Risk; awaiting Walmart backend correction  
**Last reviewed:** November 6, 2026  
**Owner:** Wesley Quintero  
**Walmart case:** [#16866157](https://seller.walmart.com/supporthub/your-cases/case-details?caseNumber=16866157)  
**Asana:** [Resolve Walmart WFS Phantom Inbound Shipment 8862220WFA](https://app.asana.com/1/1211857003594679/project/1213836032340905/task/1220010725209075)

## Issue

An accidentally created WFS shipping plan remains in Seller Center as an expected inbound shipment even though HA did not physically ship the inventory. Seller Center blocks cancellation/deletion.

- **Shipping Plan ID:** HUN-1781878717671
- **Shipment ID:** 8862220WFA
- **Destination:** IND3, 5756 Enterprise Dr, McCordsville, IN 46055
- **Ship-from shown:** 16155 W Elwood St, Goodyear, AZ 85338
- **Carrier shown:** WFS-FedEx
- **Created:** June 19, 2026
- **Estimated delivery:** June 26, 2026
- **Units shown shipped:** 918
- **Units received:** 0
- **Seller Center status:** Awaiting transit
- **Physical shipment:** None; the plan was created accidentally by a previous team member.

## Business impact

The phantom 918-unit inbound record may distort WFS inventory visibility, replenishment decisions, and forecast planning by making inventory appear to be on the way.

## Support history

- **Oct 29:** Case #16866157 submitted; Walmart acknowledged and escalated internally.
- **Oct 30:** Walmart advised an update was expected on or before Nov 8, 2026.
- **Nov 2:** Walmart reported feedback from an initial internal team and coordination with another specialized team.
- **Nov 3:** Walmart said the specialized team had not yet provided findings.
- **Nov 4:** Walmart again said no specialized-team update was available; case remained under review. Support said no seller action was required at that time.
- **Nov 5:** HA followed up requesting substantive findings, an explanation for the 918-unit shipped quantity despite no physical shipment, confirmation of backend correction status, and confirmation that the Nov 8 update commitment remained on track.
- **Nov 6 review:** The latest Walmart response visible in the case history supplied by HA remains the Nov 4 reply. No backend correction, cancellation, carrier-booking finding, or resolution has been confirmed.

## Requested resolution

1. Remove, cancel, or deactivate the incorrect shipping plan and associated inbound record through Walmart's backend.
2. Ensure the 918 units are no longer treated as expected inbound inventory.
3. Correct or refresh inventory reporting.
4. Confirm whether historical inventory or forecasting data needs to be refreshed.
5. Confirm whether any seller-side action is required after correction.

## Next steps

- Keep the case open and At Risk while Walmart investigates.
- Await Walmart's promised update by **Nov 8, 2026**; follow up if no substantive update arrives.
- If direct cancellation is unavailable, request backend correction/deactivation.
- After Walmart confirms correction, verify that the 918 units no longer appear in WFS inbound inventory, inventory reports, or replenishment/forecast planning.
- Do not treat this as a physical shipment or create a duplicate shipment to compensate for the phantom record.

## Related records

- [Walmart case #16866157](https://seller.walmart.com/supporthub/your-cases/case-details?caseNumber=16866157)
- [WFS shipping plan HUN-1781878717671](https://seller.walmart.com/wfs/shipments/order-details/HUN-1781878717671)
- [Asana task](https://app.asana.com/1/1211857003594679/project/1213836032340905/task/1220010725209075)
