<!-- HA Operations shared navigation -->
[HA Operations](../README.md) · [Projects Index & Rules](./README.md) · [R6 Rock](./R6-logistics-optimization.md) · [R6 Progress Log](./R6-update-log.md) · [Shipment Comparison Audit](./shipment-comparison-workbook-audit.md)

---
# Freight Forwarder RFQ Request Playbook

**Owner:** Wesley Quintero  
**Purpose:** A reusable, clear process for requesting comparable freight quotations from forwarders and logistics providers for Hungry Artisan.  
**Related references:** [RFQ Knowledge Base](../FF/RFQ-KB.md) · [Shipment Comparison Workbook Audit](./shipment-comparison-workbook-audit.md)  
**Status:** Active — validate shipment-specific details before sending each request.

## 1. What to ask for

For each relevant shipment, ask the provider to quote **both options** where they can support them:

1. **DDP / delivered all-in quote:** Request the full delivered price to the named destination, with a clear list of what is included and excluded. Ask the provider to identify the party responsible for import entry, duties, taxes, and any other import charges. Do not assume “DDP” automatically means every charge is included.
2. **Logistics-only quote:** Request an itemized breakdown of transportation and service charges, with customs brokerage, duties/tariffs, taxes, cargo insurance, and final-mile delivery explicitly marked as included, excluded, or separately priced.

This two-option approach helps compare the full delivered cost against a more itemized logistics option. Compare equivalent service scopes rather than comparing headline prices alone.

## 2. Prepare the shipment details

Before sending an RFQ, confirm the latest supplier and shipment records. Do not assume an old quote or previous shipment has identical specifications.

| Field | Current reference / instruction |
|---|---|
| Shipment references | FX260906 and FX260920; confirm which reference(s) the RFQ covers |
| Pickup location | Jieyang, Guangdong 522000, China — confirm the exact factory address and pickup readiness with the supplier |
| Origin port / routing | Ask the forwarder to recommend and confirm the suitable port and routing; do not assume a port without validation |
| Container / mode | Ask the forwarder to validate the proposed container configuration and quote the appropriate mode; confirm FCL, LCL, or other mode against current cargo details |
| Cargo description | Use the current commercial invoice, packing list, and product description |
| Cartons, units, dimensions, gross weight, CBM | Obtain current, shipment-specific figures from supplier documents; do not estimate if unavailable |
| Cargo value | Use the current commercial invoice value and currency |
| Destination | Name the exact receiving facility and address for the requested route; if not finalized, state that clearly and request destination-specific assumptions |
| Required timing | Provide supplier cargo-ready date and any delivery deadline, if known |
| Incoterm / service scope | Request DDP and logistics-only options and require the provider to state the applicable Incoterm and service boundaries |

**Important:** The RFQ Knowledge Base contains a current China-to-US/AWD reference, but shipment details and destinations can change. Reconcile the request against the latest supplier documents and intended route before sending.

## 3. Email template — initial RFQ request

Copy this template and replace the bracketed fields before sending.

---

**Subject:** RFQ Request — Hungry Artisan — [Shipment 1 / Shipment 2] — China to [Destination]

Hi [Name],

We are requesting a quotation for an upcoming Hungry Artisan shipment and would appreciate your recommended routing and pricing.

**Shipment details**
- **Shipment label:** [Shipment 1 / Shipment 2 — use a neutral label only; do not include an internal PO number, invoice number, or internal shipment ID]
- **Pickup location:** [Exact factory address], Jieyang, Guangdong 522000, China
- **Cargo description:** [Product description]
- **Cargo-ready date:** [Date or “to be confirmed”]
- **Total cartons / units:** [Quantity]
- **Total gross weight:** [kg]
- **Total volume:** [CBM]
- **Cargo value and currency:** [Value]
- **Destination:** [Full warehouse / 3PL / Amazon facility address, or “pending confirmation”]

Please validate the pickup point, suitable port of loading, routing, container configuration, and destination delivery requirements based on the shipment details. If any information is missing to provide a reliable quote, please list the exact items you need us to confirm.

**Please quote both of the following options, where available:**

**Option A — DDP / delivered all-in**
- Total price and pricing basis (per shipment, container, CBM, kg, or unit)
- Named delivery point and confirmation of whether final-mile delivery is included
- Clear list of included services and excluded charges
- Explicit treatment of customs clearance, duties, tariffs, taxes, bonds, inspections, and other import-related charges
- Any conditions or assumptions that could change the final price

**Option B — Logistics-only / itemized**
Please itemize the applicable charges, including:
- Origin pickup / trucking
- Export customs clearance and origin handling
- Main freight
- Destination terminal / handling charges
- Customs brokerage, entry filing, ISF or other applicable filings, and bond
- Duties, tariffs, taxes, and other government charges (state whether included or excluded)
- Cargo insurance
- Port-to-warehouse or final-mile delivery
- Any handling, inspection, documentation, appointment, or other surcharges

For both options, please also provide:
- Recommended routing and mode, including port of loading and discharge where applicable
- Estimated transit time and expected total door-to-door lead time
- Quote validity and expected sailing / departure frequency
- Payment terms and any minimum charges
- Free-time terms, demurrage/detention exposure, and major accessorial charges where applicable
- Any assumptions, exclusions, or shipment information still required

Please identify any charges that are estimates or subject to confirmation. We are collecting quotations for evaluation and comparison only; this request is not a booking instruction or commitment to award the shipment.

Thank you for your help. We look forward to reviewing your quotation.

Best regards,  
Wesley Quintero  
Hungry Artisan

---

## 4. Short follow-up message

Use this when a provider has acknowledged the request but has not sent a complete quote.

Hi [Name],

Thank you for the update. To help us compare options consistently, could you please share the quotation for [shipment reference] with both the DDP / delivered all-in option and the itemized logistics-only option, if available?

Please also confirm the proposed routing and container configuration, estimated transit time, quote validity, and which customs, duty/tax, insurance, and final-delivery charges are included or excluded. If you need any missing shipment details from us, please list them and we will coordinate with the supplier.

This is for quotation comparison only and does not authorize a booking.

Best regards,  
Wesley

## 5. How to review a quote when it arrives

Do not mark a quote as received until an actual quotation has arrived. Once received:

1. Save the quotation and record the date received, provider, shipment reference, quote reference, and expiration date.
2. Check that the quote matches the requested pickup, destination, cargo volume/weight, and container or mode.
3. Record DDP and logistics-only pricing separately. Capture the stated Incoterm and pricing basis.
4. Mark each cost component as **included**, **excluded**, **separately quoted**, or **unclear**. Follow up on unclear items before comparing totals.
5. Confirm customs clearance, duties/tariffs, taxes, insurance, and final-mile delivery responsibility in writing.
6. Capture transit time, routing, payment terms, quote validity, free time, and material surcharges.
7. Enter verified inputs into the [Shipment Logistics Comparison workbook](https://docs.google.com/spreadsheets/d/1kHKgk26CfQT1QtTZmA09Qf7l5dMD5mijonewIB6E1Ug/edit?gid=100#gid=100).
8. Compare normalized total cost and service scope against AGL and other providers. Include relevant Amazon ecosystem impacts separately rather than assuming the lowest freight quote is the lowest total cost.

## 6. RFQ completeness checklist

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

## 7. Guardrails

- A request for quotation is **not** authorization to book, pay, or commit to a provider.
- Never infer that duties, taxes, customs clearance, insurance, or delivery are included just because a quote is described as “all-in” or “DDP”; get the scope in writing.
- Do not supply guessed shipment dimensions, weights, cargo values, delivery addresses, or readiness dates. Mark them pending and ask what the provider needs.
- Ask a customs broker or qualified specialist to confirm classification, duties/tariffs, and import compliance requirements.
- Keep confirmed facts, provider estimates, assumptions, and unresolved questions distinguishable in the comparison workbook.

**Working principle:** One standardized request, two pricing views, explicit inclusions/exclusions, and no booking commitment. This keeps vendor outreach clear and makes quotes easier to compare.
