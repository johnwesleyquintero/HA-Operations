# STOCK HEALTH · STOCK AND DAYS OF COVER BY PRODUCT AND CHANNEL

> **Purpose:** Working snapshot of forecast, sales, available stock, inbound units, days of cover, and recommended transfers by product and channel.
>
> **Use:** Review channel-level shortages and warehouse stock pools before sending inventory. Treat this as the supplied snapshot; verify live inventory, shipment status, and current forecasts before acting.
>
> **Important:** Blank cells mean no value was supplied. `n/a` means the metric is not tracked for that row. Do not treat blanks as zero.

## How to read this file

- **Channel rows** show the channel's current supply and estimated days of cover.
- **Pool rows** show inventory held at the shared warehouse available to send to downstream channels.
- **Total rows** summarize stock across the country for that product.
- **Units to send** and **Status** are supplied recommendations/statuses from the source snapshot, not independently recalculated here.
- **US shared warehouse:** AWD supports Amazon US, Walmart US, and TikTok; Shopify orders draw on US stock.
- **Canada:** Proline (CA 3PL) is the warehouse for Amazon Canada.
- **United Kingdom:** SSD Logistix is the warehouse for Amazon UK.

## United States · AWD is the warehouse for Amazon, Walmart, and TikTok

| Country | Product | Channel | Forecast this month | Forecast next month | Forecast per day | Sold last 30 days | Forecast vs sold | Available | Inbound / in transit | Channel stock | Days of cover | Target days | Units to send | Send from | Status | Row type | Key | Note |
|---|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---|---|---|---|
| US | Classic FM | Amazon US | 3,875 | 4,770 | 141.7 | 4,076 | -5% | 6,167 | 457 | 6,624 | 47 | 60 | 1,884 | AWD | Below target | channel | B08BKKQ2NL | AWD auto-replenishment is on for this ASIN: Amazon moves AWD stock to FBA itself |
| US | Classic FM | Walmart US | 279 | 360 | 10.5 | 81 | +244% | 107 | 2 | 109 | 10 | 60 | 522 | AWD | Under 30 days | channel | 15315868904 | |
| US | Classic FM | TikTok | 93 | 120 | 3.5 | 5 | +1760% | 255 | 54 | 309 | 88 | 60 | 0 | AWD | OK | channel | XH-0GWW-H0T3 | |
| US | Classic FM | Shopify | 93 | 150 | 4.0 | | | | | n/a | | | | | | demand | | Stock not tracked: Shopify orders draw on US stock |
| US | Classic FM | AWD | | | | | | 0 | 10,806 | 10,806 | | | 2,406 | | Short by 2,406 units | pool | B08BKKQ2NL | |
| US | Classic FM | All US stock | 4,340 | 5,400 | 159.7 | 4,162 | | | | 17,848 | 112 | | | | OK in total | total | | |
| US | Compact FM | Amazon US | 899 | 1,950 | 46.7 | 50 | +1698% | 0 | 50 | 50 | 1 | 60 | 2,760 | AWD | OUT | channel | B0DZ74BS2D | AWD auto-replenishment is on for this ASIN: Amazon moves AWD stock to FBA itself |
| US | Compact FM | Walmart US | 310 | 420 | 12.0 | 87 | +256% | 116 | 0 | 116 | 10 | 60 | 608 | AWD | Under 30 days | channel | 15871424462 | |
| US | Compact FM | TikTok | 124 | 150 | 4.5 | 46 | +170% | 103 | 0 | 103 | 23 | 60 | 168 | AWD | Under 30 days | channel | XH-0GWW-H0T5 | |
| US | Compact FM | Shopify | 62 | 120 | 3.0 | | | | | n/a | | | | | | demand | | Stock not tracked: Shopify orders draw on US stock |
| US | Compact FM | AWD | | | | | | 0 | 7,080 | 7,080 | | | 3,536 | | Short by 3,536 units | pool | B0DZ74BS2D | |
| US | Compact FM | All US stock | 1,395 | 2,640 | 66.1 | 183 | | | | 7,349 | 111 | | | | OK in total | total | | |
| US | Premium FM | Amazon US | 1,488 | 2,640 | 67.7 | 864 | +72% | 2,711 | 187 | 2,898 | 43 | 60 | 1,164 | AWD | Below target | channel | B0DVGW1DPG | AWD auto-replenishment is on for this ASIN: Amazon moves AWD stock to FBA itself |
| US | Premium FM | Walmart US | 248 | 270 | 8.5 | 0 | | 0 | 0 | 0 | 0 | 60 | 510 | AWD | OUT | channel | 17393001155 | |
| US | Premium FM | TikTok | 310 | 360 | 11.0 | 16 | +1838% | 161 | 36 | 197 | 18 | 60 | 468 | AWD | Under 30 days | channel | XH-0GWW-H0T4 | |
| US | Premium FM | Shopify | 62 | 90 | 2.5 | | | | | n/a | | | | | | demand | | Stock not tracked: Shopify orders draw on US stock |
| US | Premium FM | AWD | | | | | | 168 | 7,902 | 8,070 | | | 2,142 | | Short by 1,974 units | pool | B0DVGW1DPG | |
| US | Premium FM | All US stock | 2,108 | 3,360 | 89.6 | 880 | | | | 11,165 | 125 | | | | OK in total | total | | |
| US | Canning Kit | Amazon US | 527 | 930 | 23.9 | 373 | +41% | 916 | 269 | 1,185 | 50 | 60 | 252 | AWD | Below target | channel | B0CCSMDSY9 | AWD auto-replenishment is on for this ASIN: Amazon moves AWD stock to FBA itself |
| US | Canning Kit | Walmart US | 651 | 1,020 | 27.4 | 348 | +87% | 323 | 1,044 | 1,367 | 50 | 60 | 288 | AWD | Below target | channel | 15316364683 | |
| US | Canning Kit | TikTok | 62 | 210 | 4.5 | 43 | +44% | 0 | 144 | 144 | 32 | 60 | 132 | AWD | OUT | channel | YI-V2Z1-U09T | |
| US | Canning Kit | Shopify | 93 | 120 | 3.5 | | | | | n/a | | | | | | demand | | Stock not tracked: Shopify orders draw on US stock |
| US | Canning Kit | AWD | | | | | | 1,656 | 0 | 1,656 | | | 672 | | Enough to cover the sends | pool | B0CCSMDSY9 | |
| US | Canning Kit | All US stock | 1,333 | 2,280 | 59.2 | 764 | | | | 4,352 | 73 | | | | OK in total | total | | |
| US | Milling Disc Expansion Set | Amazon US | 31 | 30 | 1.0 | 21 | +48% | 131 | 0 | 131 | 131 | 60 | 0 | AWD | OK | channel | B0G62PQZ4G | AWD auto-replenishment is on for this ASIN: Amazon moves AWD stock to FBA itself |
| US | Milling Disc Expansion Set | Shopify | 0 | 0 | 0.0 | | | | | n/a | | | | | | demand | | Stock not tracked: Shopify orders draw on US stock |
| US | Milling Disc Expansion Set | AWD | | | | | | 192 | 0 | 192 | | | 0 | | | pool | B0G62PQZ4G | |
| US | Milling Disc Expansion Set | All US stock | 31 | 30 | 1.0 | 21 | | | | 323 | 323 | | | | OK in total | total | | |

## Canada · Proline is the warehouse for Amazon Canada

| Country | Product | Channel | Forecast this month | Forecast next month | Forecast per day | Sold last 30 days | Forecast vs sold | Available | Inbound / in transit | Channel stock | Days of cover | Target days | Units to send | Send from | Status | Row type | Key | Note |
|---|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---|---|---|---|
| CA | Classic FM | Amazon CA | 744 | 600 | 22.0 | 129 | +477% | 1,192 | 26 | 1,218 | 55 | 60 | 108 | Proline (CA 3PL) | Below target | channel | B08BKKQ2NL | |
| CA | Classic FM | Proline (CA 3PL) | | | | | | 1,152 | 0 | 1,152 | | | 108 | | Enough to cover the sends | pool | B08BKKQ2NL | |
| CA | Classic FM | All CA stock | 744 | 600 | 22.0 | 129 | | | | 2,370 | 108 | | | | OK in total | total | | |
| CA | Premium FM | Amazon CA | 217 | 300 | 8.5 | 168 | +29% | 459 | 36 | 495 | 58 | 60 | 18 | Proline (CA 3PL) | Below target | channel | B0DVGW1DPG | |
| CA | Premium FM | Proline (CA 3PL) | | | | | | 1,296 | 0 | 1,296 | | | 18 | | Enough to cover the sends | pool | B0DVGW1DPG | |
| CA | Premium FM | All CA stock | 217 | 300 | 8.5 | 168 | | | | 1,791 | 211 | | | | OK in total | total | | |
| CA | Compact FM | Amazon CA | 186 | 360 | 9.0 | 210 | -11% | 689 | 81 | 770 | 86 | 60 | 0 | Proline (CA 3PL) | OK | channel | B0DZ74BS2D | |
| CA | Compact FM | Proline (CA 3PL) | | | | | | 288 | 0 | 288 | | | 0 | | | pool | B0DZ74BS2D | |
| CA | Compact FM | All CA stock | 186 | 360 | 9.0 | 210 | | | | 1,058 | 118 | | | | OK in total | total | | |

## United Kingdom · SSD Logistix is the warehouse for Amazon UK

| Country | Product | Channel | Forecast this month | Forecast next month | Forecast per day | Sold last 30 days | Forecast vs sold | Available | Inbound / in transit | Channel stock | Days of cover | Target days | Units to send | Send from | Status | Row type | Key | Note |
|---|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|---|---|---|---|
| UK | Classic FM | Amazon UK | 465 | 450 | 15.0 | 177 | +163% | 406 | 25 | 431 | 29 | 60 | 474 | SSD (UK 3PL) | Under 30 days | channel | B08BKKQ2NL | |
| UK | Classic FM | SSD (UK 3PL) | | | | | | 0 | 0 | 0 | | | 474 | | Short by 474 units | pool | B08BKKQ2NL | |
| UK | Classic FM | All UK stock | 465 | 450 | 15.0 | 177 | | | | 431 | 29 | | | | Under 30 days in total | total | | |

## Related files

- [Root command center](../README.md) — navigation and current priorities.
- [Inventory Health: Weekly Monitoring Routine (OPS-10)](https://docs.google.com/document/d/1M985nXeeRt6nDz8EzLmcQEhs7rrWI2PETYlHwnFNOJU/edit?tab=t.0)
- [Demand Forecasting & Reorder Triggers (OPS-11)](https://docs.google.com/document/d/1GL_v1Ceo2cR_FR8aWRlwSFr6USaFdDauUIWwaxW5dBs/edit?tab=t.0)
- [HA Inventory Plan](https://docs.google.com/spreadsheets/d/1pzVXLu4Woje4T-nETeaNULH0pPAdaMJ1infnsxzyy7E/edit?gid=1155215638#gid=1155215638)

