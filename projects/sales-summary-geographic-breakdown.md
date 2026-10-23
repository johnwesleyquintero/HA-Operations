# Sales Summary — U.S. Geographic Distribution Follow-up

**Status:** Follow-up needed  
**Owner:** Wesley  
**Requested by:** Victoria  
**Source report:** [Hungry Artisan — Sales Report (Looker Studio)](https://datastudio.google.com/reporting/01101993-6f07-4818-a7ec-2068fee48dc6/page/eGTBG)  
**Source data last updated:** October 24, 2026, 2:34 AM (as displayed in report)

## Request from Victoria

Victoria reviewed the sales report and said she liked the map. She requested the following refinements:

1. Filter the map to the **United States** and review the locations.
2. Classify **Portland in the West region**.
3. Add percentage breakdowns by **Region and State** for each SKU and for total sales, to make geographic distribution easier to compare.

This document tracks the follow-up; it does not mean the report changes have already been made.

## Current report

The existing report includes Product Sales by Location and Product Sales by Year, with a product filter that affects both views.

- [Open the sales report](https://datastudio.google.com/reporting/01101993-6f07-4818-a7ec-2068fee48dc6/page/eGTBG)

## Work plan

- [ ] Open the report and confirm the underlying data source, location fields, and available geography dimensions.
- [ ] Apply a U.S.-only filter to the map and verify that non-U.S. locations are excluded.
- [ ] Review plotted locations and correct the region mapping so **Portland is assigned to West**. Confirm which Portland location is represented in the source data before changing the mapping.
- [ ] Add a Region percentage table: one row per region, columns for each SKU, plus Total.
- [ ] Add a State percentage table: one row per state, columns for each SKU, plus Total.
- [ ] Validate percentage denominators and totals, including how blank or unmapped locations are handled.
- [ ] Review the revised map and tables with Victoria and Justin; record any further changes.

## Percentage calculation rules

Use the same U.S.-filtered sales scope as the map.

For each SKU and region/state:

**Geographic share for a SKU** = sales for that SKU in the region/state ÷ U.S. sales for that SKU × 100.

**Geographic share of total sales** = all-product sales in the region/state ÷ U.S. sales for all products × 100.

- Each SKU column should total approximately **100%** across the included regions or states, subject to rounding and any documented exclusions.
- The Total column should total approximately **100%** across regions or states.
- Region and State percentages use their own level's geographic grouping; do not divide every SKU by overall company sales unless that is the explicitly chosen metric.
- If Victoria intends percentages to represent each location's share of overall sales instead, confirm that interpretation before finalizing the tables.

## Sales by product and year — supplied report snapshot

The figures below are transcribed from the report provided with the request. Amounts are shown as displayed; currency was not specified in the supplied excerpt.

| Product | 2025 sales | 2026 sales | Combined sales | Share of combined sales |
|---|---:|---:|---:|---:|
| Classic FM | 1,619,803.42 | 1,215,438.74 | 2,835,242.16 | 73.78% |
| Premium FM | 212,904.12 | 293,023.98 | 505,928.10 | 13.17% |
| Compact FM | 117,629.22 | 210,980.06 | 328,609.28 | 8.55% |
| Canning Kit | 115,867.06 | 54,987.49 | 170,854.55 | 4.45% |
| Milling Disc Expansion Set | 0.00 | 2,136.62 | 2,136.62 | 0.06% |
| **Grand total** | **2,066,203.82** | **1,776,566.89** | **3,842,770.71** | **100.00%** |

These product totals are context for the report, not the requested Region/State breakdown. Geographic percentages must be calculated from the report's underlying location-level data after confirming the U.S. filter and location mapping.

## Related files

- [Projects index](./README.md)
- [Root operational navigation and priorities](../README.md)
- [Reports and daily priorities](../reports/README.md)
