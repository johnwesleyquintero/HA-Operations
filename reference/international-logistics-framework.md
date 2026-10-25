# OPS-00 — International Logistics Framework

**Brand:** Hungry Artisan — *From Scratch. On Purpose.*  
**Document type:** Master reference map (not a step-by-step SOP)  
**Owner:** Operations Specialist  
**Scope:** Amazon US/CA/UK, Walmart, TikTok Shop, and Shopify  
**Source note:** Consolidated from the OPS-00 reference provided by the team. Treat role assignments, contacts, facility details, and workflow statements as working reference information; verify against the current approved SOP, live platform, and manager direction before taking action.

## Purpose

Use this page to understand how inventory moves from China into each market and fulfillment channel, which actions Operations monitors or executes, and where approval is required. The live tracker and current approved SOP remain the source of truth for individual shipments and actions.

## 1. Network map

### United States

`China supplier → Amazon Global Logistics (AGL) → Amazon Warehousing & Distribution (AWD)`

- **AGL booking:** OPS-00 says Justin/Victoria arrange the AGL booking and manage supplier coordination.
- **AWD → Amazon US FBA:** FBA is described as auto-replenished from AWD. Operations monitors inventory and replenishment health; manual overrides require prior approval.
- **AWD → Walmart WFS:** Manual outbound process; Operations executes only after approval of quantity and timing.
- **AWD → TikTok FBT:** Manual outbound process; Operations executes only after approval of quantity and timing.
- **FBA → Shopify:** Shopify orders are described as fulfilled automatically from US FBA through MapMyChannel/Webee. Operations monitors the integration and escalates issues to Juls; Juls is identified as the integration subject-matter contact.

### Canada

`China supplier → Proline Logistics Services (Vancouver, BC) → Amazon CA FBA → Canadian customers`

- Proline is the 3PL/warehouse contact for receiving and storing inventory.
- The documented replenishment flow is: create the shipment plan in Amazon CA Seller Central, download labels, send them to Proline, and track dispatch/check-in.
- OPS-00 says Justin/Victoria currently notify Proline about China inbound shipments, with Operations ownership intended to transition later. Confirm current ownership before sending advance notices.

### United Kingdom

`China supplier → SSD Logistix (UK) → Amazon UK FBA → UK customers`

- SSD Logistix is the UK 3PL/warehouse contact for receiving and storing inventory.
- The documented replenishment flow is: create the shipment plan in Amazon UK Seller Central, download labels, send them to SSD, and track dispatch/check-in.
- OPS-00 says Justin/Victoria currently notify SSD about China inbound shipments, with Operations ownership intended to transition later. Confirm current ownership before sending advance notices.

## 2. Approval and control gates

**Do not approve your own inventory movement.** Under the supplied framework, obtain Victoria or Justin's sign-off before:
- AWD outbound moves to Walmart WFS or TikTok FBT (quantity and timing).
- Manual AWD → FBA replenishment overrides.
- Advance notices or commitments to a 3PL for an inbound shipment where manager ownership/approval is required.

Other guardrails:
- Do not create duplicate shipments or appointments to clear a dashboard alert without checking the current workflow and support guidance.
- A platform status or alert is not proof that a physical shipment, carrier appointment, receipt, or reconciliation has completed.
- Record the shipment reference, quantities, dates, status, and evidence. Escalate unexplained discrepancies rather than guessing.
- Unknown logistics charges or unverified route details are **unknown**, not zero or confirmed.
- A freight quote is not a booking instruction. Do not commit a shipment without the required approval.

## 3. Operations responsibilities at a glance

| Flow / area | Operations responsibility | Reference SOP |
|---|---|---|
| China → US AWD | Monitor inbound status and escalate delays; booking is assigned to Justin/Victoria in the supplied framework | OPS-01 |
| China → Proline (Canada) | Confirm receipt and track; confirm current owner for advance notices | OPS-02 |
| China → SSD (UK) | Confirm receipt and track; confirm current owner for advance notices | OPS-03 |
| AWD → FBA | Daily monitoring; flag replenishment issues; execute approved overrides only | OPS-04 |
| Proline → Amazon CA FBA | Create labels/shipment plan, send labels to Proline, track replenishment | OPS-05 |
| SSD → Amazon UK FBA | Create labels/shipment plan, send labels to SSD, track replenishment | OPS-06 |
| AWD → Walmart WFS | Execute approved manual outbound | OPS-07 |
| AWD → TikTok FBT | Execute approved manual outbound | OPS-08 |
| Shopify / Webee | Monitor order flow and escalate integration issues to Juls | OPS-09 |
| Cross-channel inventory | Weekly health checks and monitoring | OPS-10 |
| Demand / reorder planning | Follow approved forecast and reorder triggers; managers make reorder decisions per supplied framework | OPS-11 |
| Lost, damaged, stranded inventory | Investigate and document; follow the dedicated SOP | OPS-12 |
| Shipment discrepancies / check-in issues | Reconcile planned, shipped, received, and adjusted quantities; retain evidence | OPS-13 |

## 4. SOP index

The links below open the corresponding source Google Docs. Use those documents for detailed procedures; this page is the overview and navigation map.

| ID | Topic / source SOP |
|---|---|
| [OPS-00](https://docs.google.com/document/d/1U_Ws2QpGlnyldfU2myX7UxQWHGUXM2DCpedGKWWbwBs/edit?tab=t.0) | International Logistics Framework — this reference |
| [OPS-01](https://docs.google.com/document/d/1mIM6hdynzrAET6Tb4CGqmO4s0Zd63WnmnOo84oX8ux0/edit?tab=t.0) | US Inbound: China → Amazon AWD |
| [OPS-02](https://docs.google.com/document/d/1zVfe15j8F0KY2xdAVQCFiJIXZjX2gNM9OViGmD7sNc4/edit?tab=t.0) | CA Inbound: China → Proline Logistics |
| [OPS-03](https://docs.google.com/document/d/1UI7nmsIdG41rfENaCUjEM4XXMmplH2nqdMsobOn0HtA/edit?tab=t.0) | UK Inbound: China → SSD Logistix |
| [OPS-04](https://docs.google.com/document/d/1AAzgLe3eZcystX0C9ClFJlJBL13cbnxwuHpF9QRSf2I/edit?tab=t.0) | AWD → FBA Auto-Replenishment Monitoring |
| [OPS-05](https://docs.google.com/document/d/1DowgmXQAXijX4nN3XMMgVOxq1xyU7DN-UHlW2E-IVMI/edit?tab=t.0) | Amazon CA: Proline → CA FBA Replenishment |
| [OPS-06](https://docs.google.com/document/d/1aeFEMmIL4Ug4jzXtzCTNN9pu_THeDPtLliSzgvEITBk/edit?tab=t.0) | Amazon UK: SSD Logistix → UK FBA Replenishment |
| [OPS-07](https://docs.google.com/document/d/1OB_X5bgsXxE9XOfDFXEjRIrEh1hnbqPkAXbH6sLHGzs/edit?tab=t.0) | Amazon AWD → Walmart WFS |
| [OPS-08](https://docs.google.com/document/d/1uQPr-yKt7iTpE6yUYUqM5XbMLHa9X_UdATNT5wKng6Y/edit?tab=t.0) | Amazon AWD → TikTok FBT |
| [OPS-09](https://docs.google.com/document/d/1A7Ikj9VhtxuIc3kGwIqlH8t-ifVPttIXhOv387rRECE/edit?tab=t.0) | Shopify / Webee Integration Monitoring |
| [OPS-10](https://docs.google.com/document/d/1M985nXeeRt6nDz8EzLmcQEhs7rrWI2PETYlHwnFNOJU/edit?tab=t.0) | Inventory Health: Weekly Monitoring |
| [OPS-11](https://docs.google.com/document/d/1GL_v1Ceo2cR_FR8aWRlwSFr6USaFdDauUIWwaxW5dBs/edit?tab=t.0) | Demand Forecasting & Reorder Triggers |
| [OPS-12](https://docs.google.com/document/d/1ulgPD0AXLIdQ2PmzRa9AkmGguen3FpRkbwxfisSDoVA/edit?tab=t.0) | Lost / Damaged / Stranded Inventory |
| [OPS-13](https://docs.google.com/document/d/11P3DhBHk_4tUDML33JbAcW0NsQGekZ86Jreq3MFA-zA/edit?tab=t.0) | Shipment Discrepancies & Check-In Issues |
| [OPS-REF-01](https://docs.google.com/document/d/1iCg8znKmucvhTahiN6uYmqFxTjAXp9O00a837OfsC2Y/edit?tab=t.0) | Contact Directory |
| [OPS-REF-02](https://docs.google.com/document/d/1wywZ5_SskFWb3rghDDxJNhi_iidguDJjswGDju-zuRQ/edit?tab=t.0) | Product & ASIN Master List |

## 5. Key contacts

Use the current contact directory or latest email thread to verify details before sending operational instructions.

| Contact | Function | Contact detail from supplied reference |
|---|---|---|
| Justin Hopkins | CEO; approvals/escalation | justin@hungryartisan.com |
| Victoria | General Manager; first escalation point | Email not supplied; ask Justin or use current company directory |
| Carla Mae Jaraba (Mae) | PPC & performance | cmaejaraba@gmail.com |
| Julyeen (Juls) | TikTok, social, CX; Webee escalation contact | ep.hcre.manager@gmail.com |
| Divina Andres | Product research | divinaandres.amazonva@gmail.com |
| Nox | AI Operations | Via Slack |
| Bert Abedirad | Proline Logistics Services, Canada | info@prolinelogistics.ca |
| Matt Terry | SSD Logistix, UK | office@ssdlogistix.com |
| Freight forwarder | To be confirmed | Use current approved contact/tracker |
| China supplier | Jieyang Fengxing Stainless Steel; contact to be confirmed | Verify current supplier contact |

## 6. Platforms and their purpose

- **Amazon Seller Central US / AWD console:** US FBA and AWD inventory, inbound status, replenishment, and approved outbound actions.
- **Amazon Seller Central CA:** Canadian FBA replenishment and shipment labels.
- **Amazon Seller Central UK:** UK FBA replenishment and shipment labels.
- **Walmart Seller Center:** WFS inbound planning for approved AWD outbound flows.
- **TikTok Seller Center:** FBT inbound planning for approved AWD outbound flows.
- **MapMyChannel / Webee:** Shopify → FBA fulfillment integration; Operations monitors, while Juls is the listed escalation contact.
- **Google Sheets / Drive:** Inventory/shipping trackers, operational logs, and SOP library. Confirm the correct live tracker before updating records.

## 7. Product and case-pack quick reference

| ASIN | Product | MSKU | Units per case |
|---|---|---|---:|
| B08BKKQ2NL | Classic Food Mill (3-disc) | XH-0GWW-H0T3 | 6 |
| B0DVGW1DPG | Premium Food Mill (4-disc) | XH-0GWW-H0T4 | 6 |
| B0DZ74BS2D | Compact Food Mill | XH-0GWW-H0T5 | 8 |
| B0CCSMDSY9 | Canning Kit 18-pc | YI-V2Z1-U09T | 12 |
| B0G62PQZ4G | 4-Disc Expansion Set | XH-0GWW-H0T6 | 48 |

Verify identifiers and case packs against the current Product & ASIN Master List before creating a shipment or communicating quantities.

## 8. AWD facility quick reference

The supplied OPS-00 reference lists these facility IDs and addresses. Verify the destination in the live shipment workflow before using an address for booking or carrier instructions.

| Facility ID | Address |
|---|---|
| IUTE | 16155 W Elwood St, Goodyear, AZ 85338 |
| IUSW | 8130 Caliente Rd, Hesperia, CA 92344 |
| IUSR | 1120 Mt Olive Rd, Cowpens, SC 29330 |
| IUST | 15651 Greenmount Rd, Greencastle, PA 17225 |
| IUSQ | 2125 W San Bernardino Ave, Redlands, CA 92374 |

## 9. When in doubt

1. Capture the facts: screenshot, shipment/order reference, quantities, dates, current status, and relevant correspondence.
2. Check the current approved SOP and live tracker.
3. Bring the issue to Victoria first; if Victoria is unavailable, escalate to Justin.
4. Do not guess, make an unapproved inventory move, or send an external commitment before the required approval.

**Maintenance note:** This is a reference map, not evidence that a shipment has been booked, delivered, received, reconciled, or approved. Keep it aligned with the current SOP library and contact directory; update role ownership only when confirmed.
