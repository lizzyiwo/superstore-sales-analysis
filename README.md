# Superstore Sales Performance Analysis

**Prepared by:** Elizabeth Williams (Iwo) | Data Analyst & Business Analyst | Lagos, Nigeria

[![Portfolio](https://img.shields.io/badge/Portfolio-Visit%20Site-b8924a?style=flat-square)](https://lizzyiwo.github.io/ElizabethW_data/)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/elizabeth-williams50)
[![Email](https://img.shields.io/badge/Email-Get%20In%20Touch-D14836?style=flat-square&logo=gmail)](mailto:lizzyiwo@gmail.com)

**Tools:** Microsoft Excel, Power BI (DAX, Power Query, Interactive Slicers)
**Dataset:** 5,009 orders | 4 years (2014 to 2017) | $1.10M total revenue

---

## Dashboard Previews

### Page 1 — Sales Performance Overview

![Superstore Sales Performance Dashboard](https://raw.githubusercontent.com/lizzyiwo/superstore-sales-analysis/main/Screenshots/Sales%20Performance_Dashboard.png)

> Revenue $1.10M | Profit $132.52K | Quantity 19K | Orders 5K. Visualisations include: Top Performing States by Sales (California $0.21M leads), Profit by Sub-Category (Tables highlighted as the only loss-maker), Monthly Sales Trend 2014 to 2017, and Sales by Category.

---

### Page 2 — Business Intelligence Performance

![Superstore Business Intelligence and Product Dashboard](https://raw.githubusercontent.com/lizzyiwo/superstore-sales-analysis/main/Screenshots/Product_Dashboard.png)

> Five interactive slicers (Segment, Order Year, Region, Ship Mode, Category). Visualisations: Sales by Product Name (Canon imageClass leads), Impact of Discount on Profit (scatter showing profit destruction at high discount rates), Sales by Ship Mode (Standard Class 58.66%), Sales by Segment (Consumer $558K, Corporate $343K, Home Office $199K).

---

## Overview

This project analyses four years of retail sales data from a US-based superstore chain. The output is a two-page interactive Power BI dashboard built on a cleaned Excel dataset. Both pages are fully interactive via five slicers. Every finding points to a decision that could be made immediately.

---

## Problem Statement

The superstore has grown revenue year on year but the management team does not know which parts of the business are driving profit and which are consuming it. The sales team reports strong performance in technology and furniture. The finance team is concerned that heavy discounting may be eroding margins. There is no consensus on which segments to prioritise, which shipping modes are worth their cost, or which sub-categories to retire. This analysis resolves those questions with data.

---

## Dataset

| Metric | Value |
|--------|-------|
| Total Revenue | $1,099,862 |
| Total Profit | $132,516 |
| Total Quantity | 19,044 units |
| Total Orders | 5,009 |
| Overall Profit Margin | 12.05% |
| Period | January 2014 to December 2017 |

---

## Methodology

**Excel preparation** involved cleaning the raw dataset, verifying profit calculations, standardising date formats, and building PivotTables for every analytical dimension: Category, Sub-Category, Region, Segment, Shipping Mode, Discount band, and Time Series. Every chart in the Power BI dashboard traces back to a named PivotTable in the Excel file.

**Power BI dashboard** is structured across two pages. Page 1 covers headline KPIs, top states by sales, profit by sub-category, monthly sales trend, and sales by category. Page 2 adds product-level breakdown, discount impact on profit, sales by ship mode, and the segment treemap. Both pages share five slicers for Segment, Order Year, Region, Ship Mode, and Category.

---

## Key Findings

### Category Performance

| Category | Revenue | Profit | Margin |
|----------|---------|--------|--------|
| Technology | $370,157 | $70,158 | 19.0% |
| Office Supplies | $367,858 | $54,789 | 14.9% |
| Furniture | $380,298 | $7,569 | 2.0% |

Furniture generates the most revenue of the three categories but the least profit at just 2% margin. Heavy discounting in furniture and structural losses in Tables and Bookcases explain most of this gap.

### Sub-Category Profitability

**Most profitable:** Copiers $22,403 | Phones $20,939 | Accessories $19,209 | Paper $16,285 | Chairs $13,201

**Loss-making sub-categories:**

| Sub-Category | Loss |
|--------------|------|
| Tables | ($10,997) |
| Bookcases | ($1,247) |
| Supplies | ($754) |

Tables is the single most damaging sub-category. It destroys $11K annually on revenue that appears healthy on the surface. The loss is systematic, not seasonal.

### Regional Performance

| Region | Sales | Share |
|--------|-------|-------|
| West | $332,444 | 30.2% |
| East | $330,695 | 30.1% |
| Central | $246,315 | 22.4% |
| South | $190,409 | 17.3% |

California leads all states at $0.21M, followed by New York at $0.15M. West and East together generate 60% of total revenue.

### Customer Segment Analysis

| Segment | Revenue | Share |
|---------|---------|-------|
| Consumer | $558,251 | 50.8% |
| Corporate | $342,603 | 31.1% |
| Home Office | $199,009 | 18.1% |

### Shipping Mode

| Ship Mode | Revenue | Profit | Share |
|-----------|---------|--------|-------|
| Standard Class | $645,157 | $77,783 | 58.66% |
| Second Class | $222,054 | $26,925 | 20.19% |
| First Class | $169,659 | $25,887 | 15.43% |
| Same Day | $62,992 | $1,921 | 5.73% |

### Discount Impact on Profit — The Most Critical Finding

| Discount Level | Profit Contribution |
|----------------|---------------------|
| 0% | $149,265 |
| 10% | $4,811 |
| 20% | $45,534 |
| 30% | ($5,130) |
| 40% | ($10,941) |
| 50% | ($12,956) |
| 80% | ($20,018) |

Zero-discount orders generate $149,265 in profit — 113% of the reported total. The discounting strategy destroys $16,749 of profit that would otherwise be kept. The tipping point is between 20% and 30%. Every band above 30% produces a net loss.

**The business is profitable despite its discount strategy, not because of it.**

---

## Recommendations

**Retire or reprice Tables and Bookcases.** Tables loses $10,997 on revenue that looks healthy. Discontinue the highest-discount SKUs within Tables or reprice to cover costs.

**Cap discounts at 20% across all categories.** 20% is the last band at which the business remains profitable in aggregate. A policy capping promotional rates at 20% with Finance sign-off for exceptions would recover approximately $16,749 per equivalent sales cycle — a 12.6% improvement on total profit.

**Prioritise Corporate segment growth.** Corporate customers place larger orders with less promotional sensitivity than Consumer. A dedicated Corporate account management programme in the West and East regions has the highest expected return per dollar invested.

**Invest in the West and East regions.** With 60% of revenue here and California and New York as clear leaders, any investment in marketing or fulfilment in these markets has the highest marginal return.

**Review Same Day shipping economics.** At 5.73% of orders and the lowest profit of any shipping mode, Same Day pricing may not be recovering its fulfilment cost. Restrict it to high-AOV orders or reprice accordingly.

---

## File Structure

```
superstore-sales-analysis/
├── Superstore_analysis_workbook.xlsx
│   ├── Cleaned_Data
│   ├── Category
│   ├── Sub-Category
│   ├── Region
│   ├── Segment
│   ├── Discount
│   ├── Shipping Mode
│   ├── Time Series
│   ├── Total Orders
│   └── Dashboard
├── Screenshots/
│   ├── Sales Performance_Dashboard.png
│   └── Product_Dashboard.png
└── README.md
```

---

## About Elizabeth Williams

I am a Data Analyst and Business Analyst based in Lagos, Nigeria, with over five years of professional experience in financial management and accounting. This project was built to demonstrate proficiency in Excel-based data preparation, PivotTable analysis, DAX measures, and Power BI interactive dashboard design.

**Portfolio:** [lizzyiwo.github.io/ElizabethW_data](https://lizzyiwo.github.io/ElizabethW_data/)
**LinkedIn:** [linkedin.com/in/elizabeth-williams50](https://www.linkedin.com/in/elizabeth-williams50)
**Email:** [lizzyiwo@gmail.com](mailto:lizzyiwo@gmail.com)
**GitHub:** [github.com/lizzyiwo](https://github.com/lizzyiwo)
