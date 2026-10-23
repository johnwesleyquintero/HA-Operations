# Address Reference — Shipping Origins, 3PLs & Fulfillment Destinations

> **Purpose:** Reusable address reference for shipment planning, labels, routing, and marketplace inbound workflows. Compiled from the address list supplied for this document; addresses have not been independently validated.

**Last compiled:** October 24, 2026  
**Source of truth:** Verify the destination/origin against the current marketplace shipment plan, approved SOP, booking instructions, and latest supplier/3PL documents before creating labels or booking freight.

## Address directory

| Company / Facility | Address | Country | Email | Use case |
|---|---|---|---|---|
| Jieyang Fengxing Stainless Steel Products Co., Ltd | Jieyang Fengxing Stainless Steel Products Co., Ltd<br>Qi-Ning Industrial Zone<br>Jieyang, Guangdong 522000<br>China<br>Phone: (86) 663-8738 387 | China | — | Ship-from China address |
| Guangdong Minjun Trading Co., Ltd. | Guangdong Minjun Trading Co., Ltd.<br>98 Mojiang Road<br>Yangjiang City, Guangdong 529500<br>China<br>Phone: 86 13421218080 | China | — | Ship-from China address |
| Proline Logistics Services | Bert Abedirad<br>310-7330 Salisbury Ave<br>Burnaby, British Columbia V5E 4N8<br>Canada<br>Phone: (604) 500-2055 | Canada | info@prolinelogistics.ca | Ship-from Canada 3PL |
| Rivera Air Freight | Enriched Products, LLC C/O Rivera Air Freight<br>145 West 134th Street<br>Unit B<br>Los Angeles, California 90061<br>United States<br>Phone: (310) 330-3400 | United States | info@riverafreight.com | Ship-from and ship-to |
| 3PLGuys | Enriched Products, LLC C/O 3PLGuys<br>14512 Garfield Ave<br>Paramount, California 90723<br>United States<br>Phone: 8083218000 | United States | — | Ship-from address |
| Amazon AWD — IUSR | IUSR<br>1120 Mt Olive Rd<br>Cowpens, SC 29330<br>United States | United States | — | Ship-from and ship-to |
| Amazon AWD — IUST | IUST<br>15651 Greenmount Rd<br>Greencastle, PA 17225<br>United States | United States | — | Ship-from and ship-to |
| Amazon AWD — IUTE | IUTE<br>16155 W Elwood St<br>Goodyear, AZ 85338<br>United States | United States | — | Ship-from and ship-to |
| Amazon AWD — IUTL | IUTL<br>24405 Krameria Ave<br>Moreno Valley, CA 92551<br>United States | United States | — | Ship-from and ship-to |
| Amazon AWD — IUSF | IUSF<br>3351 Balmorhea Dr.<br>Dallas, TX 75241<br>United States | United States | — | Ship-from and ship-to |
| Amazon AWD — IUSJ | IUSJ<br>36900 West 4th Street<br>Beaumont, CA 92223<br>United States | United States | — | Ship-from and ship-to |
| Amazon AWD — IUSL | IUSL<br>600 Principio Pkwy W<br>North East, MD 21901-2914<br>United States | United States | — | Ship-from and ship-to |
| Amazon AWD — IUSW | IUSW<br>8130 Caliente Rd<br>Hesperia, CA 92344<br>United States | United States | — | Ship-from and ship-to |
| Amazon AWD — IUSP | IUSP<br>8140 Caliente Rd<br>Hesperia, CA 92344<br>United States | United States | — | Ship-from and ship-to |
| Amazon AWD — IUTJ | IUTJ<br>9253 Dreamland Drive<br>Fontana, CA 92335<br>United States | United States | — | Ship-from and ship-to |
| HA | TikTok Shop | FBT | TikTok Shop<br>26525 Pioneer Ave<br>Redlands, CA 92374-2052<br>United States | United States | — | Ship-to address |
| HA | TikTok Shop | FBT | TikTok Shop<br>4560 Hamner Ave<br>Eastvale, CA 91752-1038<br>United States | United States | — | Ship-to address |
| HA | Walmart WFS | Walmart WFS<br>5756 Enterprise Drive<br>McCordsville, IN 46055<br>United States | United States | — | Ship-to address |

## Use and validation rules

- **Confirm direction:** “Ship-from,” “ship-to,” and “ship-from and ship-to” describe the supplied use case, not a guarantee that a facility accepts every shipment type.
- **Validate the live shipment destination:** Amazon AWD, TikTok FBT, and Walmart WFS may assign or display destination facilities based on the specific inbound shipment. Use the destination and routing instructions generated for that shipment.
- **Check address formatting:** Preserve the company/attention line, facility code, street, unit, city, state/province, postal code, and country required by the carrier or marketplace. Do not omit a unit or facility code when one is required.
- **Do not infer missing contact details:** A dash means no email was supplied in the source list; it does not mean the facility has no email.
- **Confirm before booking:** Recheck the latest supplier/3PL instructions, pickup readiness, receiving requirements, and marketplace-generated shipment labels before tendering freight.
- **Use the appropriate SOP:** Refer to the relevant logistics SOP for China → US AWD, China → Canada 3PL, China → UK 3PL, AWD → FBA, TikTok FBT, and Walmart WFS workflows.

## Data-quality note

The supplied source listed the Amazon AWD IUSJ / Beaumont, California address three times. It is recorded once here to avoid redundant entries. Confirm that the address and facility code remain valid before using them on a live shipment.

**Important:** This is a convenience reference, not authorization to book freight or override a shipment-specific label, routing plan, or receiving instruction.
