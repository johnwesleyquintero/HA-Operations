# Marketplace Issues — SOP & Message Templates

> **Purpose:** A practical, reusable playbook for handling marketplace support issues and writing clear, human messages. Use these templates as starting points—not blind copy-and-paste scripts. Replace every placeholder, verify the evidence, and adapt the wording to the actual case.

## Operating Principles

Our support messages should sound like a capable operator speaking directly to another person—not like a legal notice or an automated escalation.

1. **Lead with the issue.** State the shipment, product, order, or transaction and the exact problem.
2. **Use evidence, not emotion.** Include quantities, dates, status, screenshots, invoices, tracking, and prior case references when relevant.
3. **Make one clear request.** Tell support exactly what investigation, correction, explanation, or action is needed.
4. **Be firm without being hostile.** Stay respectful, direct, and persistent. Avoid accusations, threats, sarcasm, and unnecessary legal language.
5. **Keep it human and concise.** Use natural sentences, ordinary language, and a simple thank-you. Don't add filler or repeat the entire case history.
6. **Preserve the record.** Reference previous cases and documents when needed. If a case is merged or closed without resolving the issue, explain what remains unresolved.
7. **Never claim more than the evidence proves.** Distinguish a confirmed loss from an in-progress receiving discrepancy or an unverified system record.
8. **Check current policy and eligibility.** A template does not guarantee reimbursement, removal, or a particular support outcome.

## Standard Workflow

### 1. Confirm the issue

Before opening or replying to a case, collect the relevant details:

- Marketplace and country
- Issue category
- Shipment, order, transaction, or case ID
- ASIN, FNSKU, MSKU, SKU, or product identifier as applicable
- Expected quantity and actual quantity/status
- Key dates: shipment creation, delivery, receiving, last support response
- What has already been tried or submitted
- Current Seller Central status and any investigation eligibility message

### 2. Check the evidence

Use the strongest available records for the specific issue:

- Shipment summary and contents
- AWD/FBA inventory or receiving reports
- Proof of delivery, carrier tracking, BOL, or appointment records
- Supplier invoice, packing list, carton labels, and shipping documents
- Transaction details or order records
- Screenshots showing the discrepancy or current status
- Previous case IDs and support responses

Do not attach unrelated documents. Use clear filenames and make sure screenshots show the relevant identifier and status.

### 3. Choose and customize a template

- Copy the **Subject** and **Message** separately.
- Replace all bracketed placeholders.
- Remove instructions and optional lines that do not apply.
- Confirm quantities, identifiers, dates, and policy references.
- Keep the message focused on one issue and one primary request.

### 4. Submit and track

Record the case ID, submission date, promised response date, next checkpoint, and current owner in the appropriate tracker/Asana task. Follow up when the promised response is missed or the issue remains unresolved.

### 5. Close only after validation

Do not mark an issue resolved just because support replied or a case was closed. Verify the actual outcome in the relevant inventory, shipment, transaction, listing, or account record.

---

## Quick Links

**Amazon Fulfillment Reports**
```
https://sellercentral.amazon.com/reportcentral/REIMBURSEMENTS/0
```

**Amazon Manage Support Cases**
```
https://sellercentral.amazon.com/cu/case-lobby?ref=ngs
```

---

## 1. AWD/FBA — Missing Items from Inbound

**Purpose**

Use when the shipment's shipped quantity and received/reconciled quantity do not match, and the remaining discrepancy needs investigation. Confirm that receiving is complete or that the shipment is eligible for investigation before requesting a final reconciliation or reimbursement review.

**Information to confirm**

- Shipment ID: [SHIPMENT ID]
- MSKU: [MSKU]
- ASIN/FNSKU: [ASIN / FNSKU]
- Shipped quantity: [QTY]
- Received quantity: [QTY]
- Remaining discrepancy: [QTY]
- Shipment/receiving status: [STATUS]
- Supporting evidence: [FILES]

**Subject**
```
[SHIPMENT ID] — Missing Units from Inbound ([DISCREPANCY QTY])
```

**Initial message**
```
Hi,

We're reviewing shipment [SHIPMENT ID] for [MSKU]. The shipment shows [SHIPPED QTY] units shipped and [RECEIVED QTY] units received, leaving a discrepancy of [DISCREPANCY QTY] units.

Could you please review the shipment's receiving and inventory records and help reconcile the remaining discrepancy?

I've attached [LIST OF RELEVANT DOCUMENTS/SCREENSHOTS] for reference.

If the units cannot be located, please let us know whether the shipment is eligible for reimbursement review under the applicable policy.

Thank you,
Wesley
```

**Follow-up — discrepancy remains after reconciliation**
```
Hi,

I'm following up on shipment [SHIPMENT ID]. The latest Shipment Summary still shows a discrepancy of [DISCREPANCY QTY] units for [MSKU], although [RECEIVING/RECONCILIATION STATUS].

Could you please review the receiving records and confirm where the remaining units were accounted for? If the units cannot be located, please advise on the next step for reimbursement review.

I've attached the latest shipment summary for reference.

Thank you,
Wesley
```

**AWD-specific short message**
```
Hi,

This shipment was created through AWD, but the shipment record still shows a discrepancy of [DISCREPANCY QTY] units for [MSKU].

Could you please review the AWD and fulfillment center inventory records and help reconcile the difference?

Thank you,
Wesley
```

**Notes**

- Do not describe units as lost until the evidence supports that conclusion.
- If receiving is still in progress, monitor until the applicable investigation window opens.
- Amazon may require invoices or other documents for certain investigations. Confirm the current request and upload the correct documents.

---

## 2. FBA — Request Reconciliation or Dispute Missing Units

**Purpose**

Use when Seller Central directs the operator to the FBA missing-units reconciliation/dispute workflow.

**Information to confirm**

- Shipment ID: [SHIPMENT ID]
- ASIN: [ASIN]
- FNSKU: [FNSKU]
- MSKU: [MSKU]
- Missing quantity: [QTY]

**Subject**
```
Request Reconciliation for Missing Units — [SHIPMENT ID]
```

**Message**
```
Shipment ID: [SHIPMENT ID]
ASIN: [ASIN]
FNSKU: [FNSKU]
MSKU: [MSKU]
Missing quantity: [QTY]

Hi,

Please review the missing units for shipment [SHIPMENT ID]. The shipment records show [BRIEF DESCRIPTION OF THE DISCREPANCY].

We have attached [SUPPORTING DOCUMENTS] to help verify the shipment contents and delivery.

Could you please reconcile the shipment records and advise whether any additional information is required?

Thank you,
Wesley
```

---

## 3. Warehouse Damage

**Purpose**

Use when Amazon or a fulfillment/warehouse record identifies inventory as damaged and a transaction or reimbursement record needs review.

**Information to confirm**

- Transaction ID: [TRANSACTION ID]
- SKU/FNSKU: [IDENTIFIER]
- Quantity: [QTY]
- Damage status/date: [DETAILS]

**Subject**
```
Warehouse Damage Review — Transaction [TRANSACTION ID]
```

**Message — request investigation**
```
Hi,

Could you please review transaction [TRANSACTION ID] for [SKU/FNSKU]? The record shows [QTY] units classified as warehouse damaged.

Please confirm the details of this transaction and advise whether the units qualify for reimbursement under the applicable policy.

Thank you,
Wesley
```

**Message — support says reimbursement processing has started**

Use this as a status reference, not as a message to send back to support:
```
We have begun processing your reimbursement request for Transaction ID [TRANSACTION ID].

We will continue to provide you with more updates in Seller Central.
```

---

## 4. Feedback Removal Request

**Purpose**

Use when seller feedback appears to meet the marketplace's feedback-removal criteria. Review the current policy and the exact feedback before submitting; product reviews and seller feedback are different.

**Information to confirm**

- Order ID: [ORDER ID]
- Feedback text/date: [DETAILS]
- Removal reason under current policy: [REASON]
- Relevant fulfillment details: [DETAILS]

**Subject**
```
Feedback Removal Request — Order [ORDER ID]
```

**Message**
```
Hi,

Please review the seller feedback associated with order [ORDER ID].

The feedback relates to [BRIEF FACTUAL DESCRIPTION]. Based on the order details, [EXPLAIN THE APPLICABLE FEEDBACK-REMOVAL REASON].

Could you please review the feedback against the current removal guidelines and remove it if it qualifies?

Thank you,
Wesley
```

**Example — delivery issue for an Amazon-fulfilled order**
```
Please review the feedback for Order ID [ORDER ID].

Seller-provided information:
Reason: Delivery-related feedback
Details: The order was fulfilled by Amazon, and the feedback concerns the delivery experience.

Please review whether this feedback qualifies for removal under the applicable policy.

Thank you,
Wesley
```

---

## 5. Warehouse Lost Investigation

**Purpose**

Use when inventory is recorded as lost at a fulfillment center and the relevant investigation workflow requires an FNSKU or other inventory identifier.

**Information to confirm**

- FNSKU: [FNSKU]
- ASIN/MSKU: [ASIN / MSKU]
- Quantity: [QTY]
- FC/location: [FC]
- Related shipment or transaction: [ID]

**Subject**
```
Warehouse Lost Investigation — FNSKU [FNSKU]
```

**Message**
```
Hi,

Please investigate the units associated with the following inventory record:

FNSKU: [FNSKU]
ASIN: [ASIN]
MSKU: [MSKU]
Quantity: [QTY]
Fulfillment center: [FC]

The inventory record indicates that these units are [CURRENT STATUS/REASON]. Could you please review the fulfillment center records and confirm the investigation outcome and any next steps?

Thank you,
Wesley
```

---

## 6. Inventory Discrepancy — Repeated Merging or Incomplete Investigation

**Purpose**

Use when follow-up cases are repeatedly merged or closed without addressing the specific unresolved discrepancy. Keep the tone factual and ask for a dedicated review; do not assume that case merging itself violates policy.

**Information to confirm**

- Shipment ID: [SHIPMENT ID]
- MSKU: [MSKU]
- Expected quantity: [QTY]
- Received quantity: [QTY]
- Remaining discrepancy: [QTY]
- Previous case IDs: [CASE IDS]
- Documents already submitted: [FILES]

**Subject**
```
Follow-up Required — Unresolved Inventory Discrepancy for [SHIPMENT ID]
```

**Message**
```
Hi,

We're following up on shipment [SHIPMENT ID], which still shows a discrepancy of [DISCREPANCY QTY] units for [MSKU].

Our previous cases [CASE IDS] have not resolved the discrepancy. The documents already submitted—including [LIST KEY DOCUMENTS]—show [BRIEF DESCRIPTION OF WHAT THE DOCUMENTS ESTABLISH].

Could you please arrange a review of the shipment and receiving records and address the remaining discrepancy directly?

In particular, please clarify:
1. How the fulfillment center classified the units.
2. Where the missing units were accounted for.
3. Whether any additional documentation is needed.
4. If the units cannot be located, whether they qualify for reimbursement review.

Please keep this issue under a dedicated investigation if possible, so the outstanding questions are not lost in the previous case history.

Thank you,
Wesley
```

**Notes**

- Only state that shipment contents matched the plan when the packing list, shipment records, and proof of delivery support that statement.
- If support identifies unexpected units or overages, ask for the specific receiving details and reconcile them against the shipment documents.
- Keep all prior case IDs and attachments available.

---

## 7. Shipment Receiving Delay

**Purpose**

Use when a shipment has been delivered or checked in but receiving has not progressed within the expected timeline, and the operator needs a status update.

**Information to confirm**

- Shipment ID: [SHIPMENT ID]
- Delivery date: [DATE]
- FC: [FC]
- Units shipped: [QTY]
- Units received: [QTY]
- Current status: [STATUS]
- Last movement/update: [DATE]

**Subject**
```
Receiving Status Request — Shipment [SHIPMENT ID]
```

**Message**
```
Hi,

Could you please provide an update on shipment [SHIPMENT ID] delivered to [FC] on [DELIVERY DATE]?

The shipment contains [QTY] units, and Seller Central currently shows [CURRENT STATUS / RECEIVED QTY]. The last recorded update was [LAST UPDATE DATE].

Could you please confirm whether the shipment is still being processed and whether any action is required from our side?

Thank you,
Wesley
```

---

## 8. Reimbursement Follow-up

**Purpose**

Use when a reimbursement request or investigation has been submitted but the outcome, amount, or processing status needs clarification.

**Information to confirm**

- Original case ID: [CASE ID]
- Shipment/transaction ID: [ID]
- SKU/FNSKU: [IDENTIFIER]
- Quantity/value: [DETAILS]
- Last support update: [DATE]

**Subject**
```
Follow-up on Reimbursement Review — [SHIPMENT OR TRANSACTION ID]
```

**Message**
```
Hi,

I'm following up on the reimbursement review for [SHIPMENT OR TRANSACTION ID], originally raised under case [CASE ID].

The outstanding issue is [BRIEF DESCRIPTION]. Could you please confirm the current review status and whether any additional information is needed from us?

If a decision has already been made, please share the outcome and the basis for the decision.

Thank you,
Wesley
```

---

## 9. General Case Escalation

**Purpose**

Use when the normal support response has not addressed the actual issue and a higher-level or specialized review is appropriate.

**Information to confirm**

- Existing case ID: [CASE ID]
- Issue/reference ID: [ID]
- What remains unresolved: [DETAILS]
- Previous actions and responses: [SUMMARY]
- Requested resolution: [ACTION]

**Subject**
```
Escalation Request — Case [CASE ID] — [ISSUE]
```

**Message**
```
Hi,

I'm following up on case [CASE ID] because the main issue remains unresolved.

To summarize:
- Issue: [ONE-SENTENCE DESCRIPTION]
- Actions taken so far: [BRIEF SUMMARY]
- Current status: [VERIFIED STATUS]
- Outstanding item: [WHAT STILL NEEDS TO HAPPEN]

Could you please escalate this for review by the appropriate team and confirm the next action and expected update?

We can provide any additional documentation needed.

Thank you,
Wesley
```

---

# New Template Entry

Use this format when adding a new recurring issue type. Keep the template focused on a real, repeatable need.

### [Issue Category]

**Purpose**

When to use this template and what it is intended to resolve.

**Information to confirm**

- [REQUIRED FIELD 1]
- [REQUIRED FIELD 2]
- [REQUIRED FIELD 3]

**Subject**
```
[Copy-ready subject]
```

**Message**
```
Hi,

[State the issue and relevant facts.]

[Make one clear request.]

Thank you,
Wesley
```

**Follow-up (optional)**
```
Hi,

I'm following up on [REFERENCE] because [UNRESOLVED ITEM].

Could you please [SPECIFIC NEXT ACTION] and confirm [STATUS / NEXT UPDATE]?

Thank you,
Wesley
```

**Notes**

- [Policy, timing, eligibility, or evidence cautions.]

---

## Final Pre-Send Checklist

- [ ] Correct marketplace, account, and case workflow
- [ ] Correct subject and reference IDs
- [ ] All placeholders replaced; no bracketed instructions left behind
- [ ] Quantities and dates checked against the source records
- [ ] Message describes only verified facts
- [ ] One clear request is included
- [ ] Tone is human, direct, respectful, and firm
- [ ] Relevant evidence is attached and filenames are clear
- [ ] Current policy and investigation eligibility checked
- [ ] Case ID and next follow-up checkpoint recorded

## SOP Maintenance

- Add a template only after the issue type has occurred often enough to justify reuse, or when a validated response is especially valuable.
- When a template works, preserve the useful wording and improve only what the evidence or policy change requires.
- Review policy-sensitive templates before reuse; marketplace rules and support workflows can change.
- Keep real shipment IDs, order IDs, customer information, and confidential case details out of generic templates. Use placeholders instead.
- Templates support consistent execution; operator judgment and evidence remain mandatory.
