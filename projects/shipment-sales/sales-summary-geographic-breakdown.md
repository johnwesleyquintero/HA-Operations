# Sales Summary — U.S. Geographic Distribution Follow-up

**Status:** Implemented — ready for stakeholder review; percentage scaling QA should be confirmed before treating every metric as final  
**Owner:** Wesley  
**Requested by:** Victoria  
**Source report:** [Hungry Artisan — Sales Report (Looker Studio)](https://datastudio.google.com/reporting/01101993-6f07-4818-a7ec-2068fee48dc6/page/eGTBG)  
**Last documented update:** October 27, 2026

## Request from Victoria

Victoria reviewed the sales report and said she liked the map. She requested the following refinements:

1. Filter the map to the **United States** and review the locations.
2. Classify **Portland in the West region**.
3. Add percentage breakdowns by **Region and State** for each SKU and for total sales, to make geographic distribution easier to compare.

## Implementation update

The requested report features have been implemented, and the updated report is ready for review.

- **U.S. geographic map:** The report now focuses on U.S. shipment locations.
- **Region and State percentage breakdowns:** Added a sales-share view by product, including total sales and geographic share metrics.
- **Table drill-down controls:** Added drill-down buttons to the tables to make it easier to explore the underlying geographic and sales details.
- **Report access:** [Open Hungry Artisan — Sales Report (Looker Studio)](https://datastudio.google.com/reporting/01101993-6f07-4818-a7ec-2068fee48dc6/page/eGTBG)

## Completion checklist

- [x] Add a U.S.-focused map view.
- [x] Add Region/State sales percentage breakdowns by SKU and total.
- [x] Add drill-down buttons to the tables for more detailed exploration.
- [ ] Confirm Portland's source location and verify its West region classification in the live report.
- [ ] Validate that all percentage fields use a consistent stored-value scale and display correctly in Looker Studio.
- [ ] Review the updated report with Victoria and Justin and capture any requested adjustments.

## Percentage calculation rules

Use the same U.S.-filtered sales scope as the map.

**Geographic share for a SKU** = sales for that SKU in the region/state ÷ U.S. sales for that SKU × 100.

**Geographic share of total sales** = all-product sales in the region/state ÷ U.S. sales for all products × 100.

- Each SKU column should total approximately **100%** across the included regions or states, subject to rounding and documented exclusions.
- The Total column should total approximately **100%** across regions or states.
- Region and State percentages use their own geographic grouping; do not divide every SKU by overall company sales unless that is the explicitly intended metric.
- Keep the percentage storage convention consistent across the source data and report formatting. If values are stored as decimal fractions, a value of `0.2442` should display as `24.42%`; a value of `24.42` with percent formatting would display incorrectly as `2,442%`.
- Confirm how blank or unmapped locations are handled and document any exclusions.

## Sales by product and year — earlier supplied snapshot

The figures below are retained from the earlier report snapshot for context. They are not the new Region/State breakdowns, and should not be treated as current totals without refreshing the source report.

| Product | 2025 sales | 2026 sales | Combined sales | Share of combined sales |
|---|---:|---:|---:|---:|
| Classic FM | 1,619,803.42 | 1,215,438.74 | 2,835,242.16 | 73.78% |
| Premium FM | 212,904.12 | 293,023.98 | 505,928.10 | 13.17% |
| Compact FM | 117,629.22 | 210,980.06 | 328,609.28 | 8.55% |
| Canning Kit | 115,867.06 | 54,987.49 | 170,854.55 | 4.45% |
| Milling Disc Expansion Set | 0.00 | 2,136.62 | 2,136.62 | 0.06% |
| **Grand total** | **2,066,203.82** | **1,776,566.89** | **3,842,770.71** | **100.00%** |

## Related files

- [Projects index](./README.md)
- [Root operational navigation and priorities](../README.md)
- [Reports and daily priorities](../reports/README.md)
