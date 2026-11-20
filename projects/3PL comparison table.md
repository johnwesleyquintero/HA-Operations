### How Rates Were Normalized & Mapped in the CSV:

1. **Storage Normalized to Per Week (`$/pallet/week`):**
   - **Flexport:** Quoted daily at `$2.75 / day / pallet` $\rightarrow$ normalized to `$19.25 / week` ($2.75 \times 7$). *(Includes 4 free days).*
   - **3PL Guys:** Quoted monthly at `$30.00 / month / pallet` $\rightarrow$ normalized to `$7.00 / week` ($30 / 4.286$).
   - **PCLA:** Quoted monthly at `$28.00 / month / pallet` $\rightarrow$ normalized to `$6.53 / week` ($28 / 4.286$). *(Includes first 30 days free).*
   - **California FBA Prep:** Quoted monthly at `$25.00 / month / pallet` (for $10+$ pallets) $\rightarrow$ normalized to `$5.83 / week` ($25 / 4.286$). *(Prorated daily).*

2. **Container Unloading Baseline (`40ft / 40HQ`):**
   - **Flexport:** `$490.00` (for 40ft/40HQ/45HQ receiving + unloading palletized).
   - **3PL Guys:** `$800.00` (flat rate for 40ft/40HQ/45ft floor-loaded container; their rule is *either/or* — no stacked per-carton unloading fee).
   - **PCLA:** `$550.00` (main rate card 40ft; $650 for 40ft HC, +$100 if floor-loaded surcharge applies).
   - **California FBA Prep:** `$500.00` (40ft floor-loaded, up to 1,500 boxes; exceeding boxes +$0.25/box).

3. **Inbound Palletizing / Pallet Receiving (`$/pallet`):**
   - **Flexport:** `$16.50 / pallet` (inbound palletizing, stretch-wrap included).
   - **3PL Guys:** `$15.00 / pallet` (palletized receiving).
   - **PCLA:** `$12.00 / pallet` (pallet receiving on main rate card; note: conflicts with $25 on alternate sheet).
   - **California FBA Prep:** `$15.00 / pallet` (inbound palletizing; $10.00 if already palletized).

4. **Sort / Re-Carton (`$/carton` or `$/unit`):**
   - **Flexport:** `$0.30 / carton` (non-palletized receiving fee).
   - **3PL Guys:** Included in the container flat rate (strictly *either/or* structure).
   - **PCLA:** `$0.08 / unit` (per-unit receiving itemized line).
   - **California FBA Prep:** `$0.90 / carton` (sorting mixed SKU pallet; 1–5 SKUs per container free, 5+ SKUs is $10/SKU).

5. **Channel Labeling (`$/carton`):**
   - **Flexport:** `$0.35 / label`.
   - **3PL Guys:** `$0.20 / unit` labeling.
   - **PCLA:** Bundled inside FBA prep tiers ($0.75–$1.25/unit all-inclusive).
   - **California FBA Prep:** `$0.50 / label` (outbound LTL box label fee).

6. **Outbound Pallet Build & Handling / Admin:**
   - **Outbound Pallet Build:** Flexport: `$16.50` | 3PL Guys: `$25.00` (pallet forwarding) | PCLA: `$19.00` (outbound pallet & shrink-wrap) | CA Prep: `$15.00` (new pallet build).
   - **Admin / Outbound Delivery Handling:** 3PL Guys: `$1.00 / carton` | PCLA: `$5.00` BOL fee | CA Prep: `$25.00` BOL fee (+ $10.00 pick & load).

7. **Shopify / DTC Pick & Pack (`$/order`):**
   - **PCLA:** `$1.50 / order` base tier rate.
   - **California FBA Prep:** Normalized base order at `$1.10 / order` ($0.85 order fee at 500+ daily orders tier + $0.15 order line fee + $0.10 pick fee for items under 10 lbs).
   - **Flexport & 3PL Guys:** Require dedicated custom DTC scope quoting.





| Field / Metric | Flexport | 3PL Guys | Prep Center LA (PCLA) | California FBA Prep Center | Matrix Fulfillment | Notes / Source |
| --- | --- | --- | --- | --- | --- | --- |
| Rate card Data: | `Flexport_3PL_Rate_Card.pdf` | `3plguys_pricing-2.pdf` | `PCLA-Rate-Card-Comparison-Standard-Pro-Enterprise.pdf` | `CALIFORNIA FBA PREP CENTER_SHF_Price_072026.pdf` | `To Follow` | Matched to source files |
| Hub: container unload per container ($) | `$490.00` | `$800.00` | `$550.00` | `$500.00` | — | 40ft/40HQ standard floor-loaded / palletized container unload rates |
| Hub: receive and palletize per pallet ($) | `$16.50` | `$15.00` | `$12.00` | `$15.00` | — | Standard per-pallet receiving / palletizing rate |
| Hub: sort / re-carton per carton ($) | `$0.30` | — | `$0.08` | `$0.90` | — | Flexport: $0.30/non-palletized carton; PCLA: $0.08/unit receiving; CA Prep: $0.90/carton sorting |
| Hub: channel labels per carton ($) | `$0.35` | `$0.20` | — | `$0.50` | — | Per-label / carton fee (CA Prep: $0.50 outbound LTL box label; PCLA prep includes labeling) |
| Hub: outbound pallet build per pallet ($) | `$16.50` | `$25.00` | `$19.00` | `$15.00` | — | Flexport palletizing ($16.50); 3PL Guys ($25.00 LTL pallet forwarding); PCLA ($19.00 outbound pallet & wrap); CA Prep ($15.00 new pallet build) |
| Hub: handling + admin per outbound delivery ($) | — | `$1.00` | `$5.00` | `$25.00` | — | 3PL Guys: $1.00/carton handling; PCLA: $5.00 BOL; CA Prep: $25.00 BOL fee |
| Hub: storage per pallet per week ($) | `$19.25` | `$7.00` | `$6.53` | `$5.83` | — | Normalized to weekly rate: Flexport ($2.75/day = $19.25/wk); 3PL Guys ($30/mo ≈ $7.00/wk); PCLA ($28/mo ≈ $6.53/wk); CA Prep ($25/mo ≈ $5.83/wk) |
| LTL to Amazon / Walmart / TikTok per pallet ($) | `Quote required` | `Quote required` | `Quote required` | `Quote required` | — | All rate cards explicitly note destination zip codes are required for LTL freight quoting |
| Hub 3PL pick, pack and postage ($/order) | `Quote required` | `Quote required` | `$1.50` | `$1.10` | — | PCLA: from $1.50/order; CA Prep: $0.85 order fee + $0.15 line + $0.10 pick = $1.10 (500+ tier base order) |
