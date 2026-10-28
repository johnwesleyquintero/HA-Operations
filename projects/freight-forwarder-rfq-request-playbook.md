# Freight Forwarder RFQ Request Playbook

**Owner:** Wesley Quintero  
**Purpose:** A reusable, clear process for requesting comparable freight quotations from forwarders and logistics providers for Hungry Artisan.  
**Related references:** [RFQ Knowledge Base](../FF/RFQ-KB.md) · [Shipment Comparison Workbook Audit](./shipment-comparison-workbook-audit.md)  
**Status:** Active — validate shipment-specific details before sending each request.

## 1. Outreach approach — conversation first

**Use the playbook as an internal guide, not a script every provider must receive.** Justin’s direction is to keep outreach natural and direct: providers want to understand the shipment and discuss the business, not work through a long questionnaire before they can respond.

### Step 1: Start with a short message

Open with the shipment’s origin, intended destination, and request for recommended routing and pricing. Ask whether the provider can quote a delivered option and, if available, a logistics-only breakdown. Offer to send the packing details they need.

**Example — initial message**

> Hi [Name], thanks for connecting. We have an upcoming shipment from China to [destination] and would like to get your recommended routing and pricing. Could you quote a delivered option and, if available, a breakdown of the logistics charges as well? I can send over the packing details and delivery information. Let me know what you need from our side to put together an accurate quote. Thanks, Wesley

Adapt this to the conversation. Do not send every bullet from the detailed RFQ template by default.

### Step 2: Share verified shipment details when useful

Use current supplier and shipment records. Send the information the provider needs to price the shipment; do not make them ask for details we already have verified.

| Detail | Source / instruction |
|---|---|
| Pickup location | Confirm exact factory address and readiness with the supplier; Jieyang, Guangdong 522000 is a reference, not a substitute for the exact address. |
| Cargo description, cartons, units, dimensions, gross weight, CBM | Use current packing list and supplier documents. |
| Cargo value and currency | Use the current commercial invoice internally; share only what is needed for the quote. |
| Destination | Provide the exact receiving facility and address when confirmed. If pending, say so and ask what assumptions the provider can quote against. |
| Cargo-ready date and delivery deadline | Use confirmed dates; otherwise mark pending. |
| Route, port, mode, container configuration | Ask the provider to recommend and validate against the actual cargo. |

Shipment references FX260906 and FX260920 are internal prompts to verify which load is being discussed. Use neutral external labels such as **Shipment 1** or **Shipment 2**; never expose internal PO numbers, invoice details, internal shipment IDs, or internal cost notes.

### Step 3: Clarify only what is missing

Once a quote or initial response arrives, compare it against the internal requirements in [Shipment Comparison Workbook Audit](./shipment-comparison-workbook-audit.md). Ask short, specific questions only for missing or unclear items—for example:

- “Does this price include customs clearance, duties/taxes, and delivery to the named warehouse?”
- “Could you confirm the estimated door-to-door lead time and how long this quote is valid?”
- “Are any destination, handling, appointment, or other charges billed separately?”
- “Could you also share the logistics-only breakdown, if available?”

Request both **DDP / delivered all-in** and **logistics-only / itemized** options when practical, but do not block a useful initial conversation if the provider needs to scope the shipment first. “DDP” or “all-in” is not proof that every charge is covered; obtain inclusions and exclusions in writing before comparing totals.

### Step 4: Use the detailed RFQ when appropriate

Use the detailed email template below when the provider requests a formal RFQ, the shipment is complex, several parties need the same specification, or a first quote cannot be compared without a structured request. Treat it as a reusable reference: tailor it to the provider and shipment, remove irrelevant questions, and never ask for information already supplied.

Before sending, reconcile all shipment-specific details with the latest supplier documents and intended route. Do not assume the RFQ Knowledge Base or an old quote describes the current shipment.



## 1.1 Align every RFQ to the comparison workbook

The RFQ should collect enough verified information to populate the [Shipment Logistics Comparison workbook](https://docs.google.com/spreadsheets/d/1kHKgk26CfQT1QtTZmA09Qf7l5dMD5mijonewIB6E1Ug/edit?gid=100#gid=100)—not force every provider through a generic questionnaire.

**The unit of comparison is one defined shipment/load and its intended routing.** The workbook compares the AGL baseline against up to three third-party forwarder / 3PL scenarios for that load. Keep the shipment facts, destination, cargo assumptions, and service scope consistent across the options being compared.

### Network scope

R6 covers China-origin logistics for the **US, Canada, and UK**. The relevant delivery path may involve:

- **Amazon Global Logistics (AGL) → AWD**, then onward transfer to FBA Direct, Walmart WFS, or TikTok FBT where applicable.
- **A third-party forwarder / 3PL**, with delivery to the specific applicable destination: AWD, FBA Direct, WFS, or FBT—or to a named 3PL hub when that is the route being evaluated.

Do not assume every provider serves every country, facility, or channel. Confirm capability and request pricing only for the shipment's actual destination(s). If a shipment is split across channels, share the verified allocation and request separate delivery/handling costs for each applicable destination where the provider can quote them. Do not ask a provider to price hypothetical destinations that are not part of the load unless we are deliberately running a clearly labelled scenario.

### What the quote must let us compare

For each relevant option, capture or clarify:

1. **Scope:** origin and exact destination/facility; delivery endpoint; Incoterm; mode; route; container configuration; cargo quantity, dimensions, weight, and CBM.
2. **Price basis:** total price and currency, plus rate basis/minimums; quote date, reference, and expiry.
3. **Included vs. excluded charges:** origin services, main freight, destination handling, customs/brokerage/bond, duties/tariffs/taxes, insurance, final-mile delivery, appointment/accessorial fees, and 3PL receiving/storage/handling/transfer fees where relevant.
4. **Time and commercial terms:** estimated door-to-door lead time (distinguish from port-to-port transit), departure frequency, payment terms, free time, and material surcharges.
5. **Uncertainty:** identify estimates, assumptions, and charges subject to confirmation.

A provider does **not** have to use our workbook categories or complete our internal checklist. They can reply in their own format; we map their answer into the workbook and follow up only on material gaps. Keep AGL's Amazon-specific fees and benefits in the internal baseline/rate card rather than asking an alternative forwarder to estimate them.

### Workbook cost lines — what the quote needs to clarify

The current comparison output evaluates the cost of moving **one defined shipment** through the AGL baseline and up to three alternative scenarios. Request enough information to populate the following fields without treating missing charges as free:

| Workbook line | Ask the forwarder to confirm |
|---|---|
| **Main freight / all-in quote** | Total quoted amount and currency; whether this is base ocean/air freight only or an all-in amount; rate basis, minimums, container count/type, and exactly which fees are included. Provide the base freight line separately when possible. |
| **Origin charges** | Factory pickup/trucking, export customs clearance, origin handling/terminal charges, documentation, and any other origin fees. State included, excluded, or not applicable with reason. |
| **Destination port, brokerage, insurance** | Destination terminal/handling/drayage; customs brokerage and entry filing; ISF or other applicable filing; bond; cargo insurance. Itemize each fee and identify the party responsible. Do not combine unrelated booking, documentation, or ISPS charges under destination without explaining their classification. |
| **Duty & tariff** | Duties, tariffs, taxes, inspections, and government charges: amount or calculation basis if available, what is included/excluded, and whether the quote is DDP or another Incoterm. If the forwarder cannot calculate duties, explicitly state that they are excluded and require broker confirmation. |
| **Delivery to AWD** | Final-mile delivery to the exact named Amazon Warehousing and Distribution facility, including appointment booking, delivery/receiving requirements, accessorials, and any separate charges. |
| **Delivery / transfer to FBA, Walmart WFS, TikTok FBT** | Quote only the destinations relevant to the shipment. Identify whether each service is offered and itemize delivery, transfer, appointment, and handling charges for each applicable endpoint. |
| **Inbound placement fees** | These are often marketplace/Amazon-side costs rather than forwarder charges. Ask the provider only if it claims a specific fee or service affects them; otherwise populate from the internal Amazon rate card/workbook, not a forwarder guess. |
| **Hub storage, handling & AWD fees** | If a third-party hub or 3PL is part of the route, itemize receiving, unloading, palletization, storage (rate and billing unit), pick/handling, prep, and onward delivery to AWD or other channels. State free days, minimums, and assumptions. |
| **Other fees** | Booking, documentation, AMS/ISPS, carbon offset, inspections, peak/general rate increases, fuel/security surcharges, detention/demurrage, appointment, and any other charge not already included above. Identify fee name, amount, billing basis, and cost category; avoid double-counting fees already included in freight or destination subtotals. |
| **Days: transit + to sellable** | Separate port-to-port transit from origin dwell, destination dwell, customs clearance, final-mile delivery, warehouse appointment/receiving, and estimated time until inventory is available/sellable. If the provider cannot estimate sellable timing, state the endpoint of its estimate and leave downstream time pending. |
| **Quote valid until** | Quote reference/date, expiration date, sailing/departure frequency, rate-change conditions, and any general rate increase or market surcharge caveats. |

**Comparison controls**
- Ask for both **DDP / delivered all-in** and **FOB or logistics-only itemized pricing** where available, for the same shipment scope and delivery endpoint. DDP is useful for a landed-cost scenario; FOB/logistics-only helps expose individual cost components but may leave customs, duties, and final delivery outside the quote.
- Request separate pricing for each applicable endpoint when a shipment is split. Do not assume an AWD quote also covers FBA Direct, Walmart WFS, TikTok FBT, or Shopify fulfillment.
- For Shopify orders fulfilled through Amazon MCF / AWD-to-FBA, use the internal Amazon fee source and workbook assumptions unless the provider is specifically quoting a third-party service. Do not ask freight forwarders to estimate Amazon MCF fulfillment fees.
- For every line, record one of: **quoted**, **estimated by provider**, **internal planning assumption**, **excluded**, **not applicable**, or **pending**. A blank or unquoted cost must not silently become a confirmed $0.
- Reconcile the quote's itemized lines to its stated total. If the numbers do not add up, ask the provider which lines are included before entering them in multiple workbook categories.

## 2. Detailed RFQ reference — use when needed

The template is optional and should be adapted to the conversation. Replace bracketed fields, remove non-applicable items, and do not send unverified information.

### Formal RFQ email template

Use this only when a structured request is appropriate. Replace the bracketed fields and remove anything not relevant to this shipment.

---

**Subject:** RFQ Request — Hungry Artisan — [Shipment 1 / Shipment 2] — China to [Destination]

Hi [Name],

We are requesting a quotation for an upcoming Hungry Artisan shipment and would appreciate your recommended routing and pricing.

**Shipment details**
- **Shipment label:** [Shipment 1 / Shipment 2 — use a neutral label only; do not include an internal PO number, invoice number, or internal shipment ID]
- **Pickup location:** [Verified factory address]
- **Cargo description:** [Product description]
- **Cargo-ready date:** [Confirmed date or “to be confirmed”]
- **Total cartons / units:** [Verified quantities]
- **Total gross weight / volume:** [kg / CBM from current packing data]
- **Cargo value and currency:** [Verified value, shared only as needed for quoting]
- **Destination country and delivery endpoint:** [US / Canada / UK + exact facility or 3PL address, or “pending confirmation”]
- **Fulfillment destination(s), if relevant:** [AWD, FBA Direct, Walmart WFS, TikTok FBT, or named 3PL hub]
- **Channel allocation, if split:** [Verified units/cartons allocated to each applicable destination, or “not yet confirmed”]

Please confirm that you can serve this origin, country, and named delivery endpoint. Recommend the appropriate routing, mode, port of loading/discharge, and container configuration for this cargo. Quote only the destination(s) listed above; where the load is split across channels, identify separate delivery/handling prices for each applicable endpoint if available. If any information is missing to provide a reliable quote, please list the exact items you need us to confirm.

**Please quote both of the following options, where available:**

**Option A — DDP / delivered all-in**
- Total price and pricing basis (per shipment, container, CBM, kg, or unit)
- Named delivery point and confirmation of whether final-mile delivery is included
- Clear list of included services and excluded charges
- Explicit treatment of customs clearance, duties, tariffs, taxes, bonds, inspections, and other import-related charges
- Any conditions or assumptions that could change the final price

**Option B — Logistics-only / itemized**
Please itemize the applicable charges for the same origin, cargo, route, and destination scope as Option A. Where applicable, please show separate line items for:

- Factory pickup / trucking and other origin charges
- Export customs clearance, origin handling / terminal charges, and origin documentation
- Main freight, with rate basis and container/mode details
- Booking fee, bill-of-lading/document fees, AMS/ISPS, carbon offset, and other freight-related surcharges
- Destination terminal / handling / drayage
- Customs brokerage, entry filing, ISF or other applicable filings, and bond
- Duties, tariffs, taxes, inspections, and other government charges (state whether included, excluded, or not calculated)
- Cargo insurance
- Final-mile delivery to the exact named AWD facility
- Separate delivery / transfer charges to FBA Direct, Walmart WFS, or TikTok FBT only if those endpoints are part of the requested shipment scenario
- 3PL / hub receiving, unloading, palletization, storage (include rate and billing unit), handling, prep, and onward transfer if applicable
- Appointment, accessorial, detention/demurrage, free-time, peak-season, fuel/security, general-rate-increase, or other fees

Please identify the billing basis and whether each item is included in another line or in the quoted total. We need to avoid counting the same fee twice. If a charge is excluded or unavailable, please label it as excluded / not quoted rather than leaving us to assume it is zero.

For both options, please also provide:
- Recommended routing and mode, port of loading/discharge, container configuration, and number of containers
- Estimated port-to-port transit time **and** estimated total door-to-door lead time
- Estimated origin/destination dwell, customs clearance, final-mile, appointment/receiving time, and (if you can estimate it) time until inventory is available for sale
- Quote reference/date, validity/expiry, expected sailing/departure frequency, and conditions that may change the rate
- Payment terms, minimum charges, free-time terms, and demurrage/detention exposure
- Any assumptions, exclusions, and shipment information still required

Please identify any charges that are estimates or subject to confirmation. We are collecting quotations for evaluation and comparison only; this request is not a booking instruction or commitment to award the shipment.

Thank you for your help. We look forward to reviewing your quotation.

Best regards,  
Wesley Quintero  
Hungry Artisan

---



## 3. Short, targeted follow-up

Use this when a specific material detail is still missing. Tailor the question to the gap rather than resending the full RFQ.

Hi [Name],

Thank you for the update. To help us compare options consistently, could you please share the quotation for [shipment reference] with both the DDP / delivered all-in option and the itemized logistics-only option, if available?

Please also confirm the proposed routing/container configuration, quote validity, and the included/excluded status of origin charges, destination terminal/drayage, customs/brokerage/bond, duties/tariffs/taxes, insurance, final-mile delivery to the named facility, and any 3PL receiving/storage/handling fees. Please separate port-to-port transit from total door-to-door and warehouse-to-sellable timing where available. If you need missing shipment details, list the exact items and we will coordinate with the supplier.

This is for quotation comparison only and does not authorize a booking.

Best regards,  
Wesley

## 4. How to review a quote when it arrives

Do not mark a quote as received until an actual quotation has arrived. Once received:

1. Save the quotation and record the date received, provider, shipment reference, quote reference, and expiration date.
2. Check that the quote matches the requested pickup, destination, cargo volume/weight, and container or mode.
3. Record DDP and logistics-only pricing separately. Capture the stated Incoterm and pricing basis.
4. Confirm the quote matches the exact country, facility / delivery endpoint, and channel allocation being modeled. Do not compare a port-only quote with a delivered quote as if their scope were equivalent.
5. Mark each cost component as **included**, **excluded**, **separately quoted**, or **unclear**. Follow up on unclear items before comparing totals.
6. Confirm customs clearance, duties/tariffs, taxes, insurance, and final-mile delivery responsibility in writing.
7. Capture transit time, routing, payment terms, quote validity, free time, and material surcharges.
8. Enter verified inputs into the [Shipment Logistics Comparison workbook](https://docs.google.com/spreadsheets/d/1kHKgk26CfQT1QtTZmA09Qf7l5dMD5mijonewIB6E1Ug/edit?gid=100#gid=100).
9. Compare normalized total cost and service scope against AGL and other providers for that same shipment and destination path. Include relevant Amazon ecosystem impacts separately rather than assuming the lowest freight quote is the lowest total cost.

## 5. Internal RFQ readiness checklist

- [ ] Neutral shipment label used; PO numbers, invoice numbers/details, and internal shipment IDs excluded from the external request\n- [ ] Current supplier documents confirmed internally
- [ ] Exact pickup address and cargo-ready timing confirmed or clearly marked pending
- [ ] Cartons, dimensions, CBM, gross weight, and cargo value confirmed
- [ ] Destination address confirmed or explicitly marked pending
- [ ] Provider asked to validate route, port, mode, and container configuration
- [ ] DDP / delivered all-in quote requested
- [ ] Logistics-only itemized quote requested
- [ ] Included and excluded costs clearly identified
- [ ] Transit time, validity, payment terms, and surcharges requested
- [ ] Quote saved and status updated only after it is actually received

## 6. Guardrails

- **Do not include internal PO numbers, invoice numbers, or internal PO/invoice details in any external RFQ or vendor communication.** This follows Justin’s explicit instruction.
- Do not include internal shipment IDs or internal cost/pricing notes in vendor-facing messages; use neutral labels such as **Shipment 1** and **Shipment 2** when needed. Keep the cross-reference in internal records.
- A request for quotation is **not** authorization to book, pay, or commit to a provider.
- Never infer that duties, taxes, customs clearance, insurance, or delivery are included just because a quote is described as “all-in” or “DDP”; get the scope in writing.
- Do not supply guessed shipment dimensions, weights, cargo values, delivery addresses, or readiness dates. Mark them pending and ask what the provider needs.
- Ask a customs broker or qualified specialist to confirm classification, duties/tariffs, and import compliance requirements.
- Keep confirmed facts, provider estimates, assumptions, and unresolved questions distinguishable in the comparison workbook.

**Working principle:** Keep the conversation human and direct; standardize the internal comparison. Ask for the information needed to evaluate the quote, clarify only material gaps, preserve confidentiality, and never imply a booking commitment.
