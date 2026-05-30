# Superstore Sales Performance Analysis

**Prepared by:** Elizabeth Williams (Iwo)
**Tools:** Microsoft Excel, Power BI (Power Query, DAX, Interactive Dashboards)
**Dataset:** 5,009 orders | 4 years (2014 to 2017) | \$1.10M total revenue
**Portfolio:** [lizzyiwo.github.io/ElizabethW_data](https://lizzyiwo.github.io/ElizabethW_data/)
**LinkedIn:** [linkedin.com/in/elizabeth-williams50](https://www.linkedin.com/in/elizabeth-williams50)

---

## Overview

This project analyses four years of retail sales data from a US-based superstore chain to answer the questions that matter most to a retail business: which products are actually profitable, where is the business growing and where is it shrinking, who its most valuable customers are, and what the discount strategy is doing to the bottom line. The output is a two-page interactive Power BI dashboard built on a cleaned Excel dataset, designed so that any stakeholder can filter by segment, region, year, shipping mode, and category and immediately see how the numbers change.

The analysis is not descriptive. Every section ends with a finding that points to a decision someone could make tomorrow.

---

## Problem Statement

The superstore has been operating for four years and has grown revenue year on year, but the management team does not know which parts of the business are driving profit and which are consuming it. The sales team reports strong performance in technology and furniture. The finance team is concerned that heavy discounting may be eroding margins. There is no consensus on which customer segments to prioritise, which shipping modes are worth the cost, or which product subcategories to reduce or retire. This analysis was built to resolve those questions with data rather than opinion.

---

## Dataset

The dataset contains 5,009 order records spanning January 2014 to December 2017 across the United States. Each record includes Order ID, Order Date, Ship Date, Ship Mode, Customer segment, product Category and Sub-Category, Region, Sales, Quantity, Discount, and Profit.

The data was cleaned in Excel before analysis. The Cleaned Data sheet documents the preparation steps applied: date format standardisation, profit calculation verification, and removal of null values. No records were excluded from the analysis.

**Summary statistics:**

Total Revenue: \$1,099,862
Total Profit: \$132,516
Total Quantity Sold: 19,044 units
Total Orders: 5,009
Profit Margin (overall): 12.05%

---

## Methodology

The analysis was structured in three stages: data preparation in Excel, exploratory analysis using PivotTables, and dashboard construction in Power BI.

**Excel preparation** involved cleaning the raw dataset, verifying the profit column against the formula (Sales minus (Sales multiplied by Discount) minus Cost), standardising date formats, and building the summary PivotTables that feed the analysis: by Category, Sub-Category, Region, Segment, Shipping Mode, Discount band, and Time Series.

**PivotTable analysis** was used to identify the primary profit drivers and problem areas before visualisation. Each pivot is saved as a named sheet in the workbook and forms the source of a visual in the Power BI report. This keeps the analysis traceable: every chart in the dashboard can be validated against a PivotTable in the Excel file.

**Power BI dashboard** is structured across two pages. Page one (Executive Sales Overview) covers the headline KPIs, top-performing states by sales, profit by sub-category, monthly sales trend from 2014 to 2017, and sales by category. Page two (Business Intelligence Performance and Customer and Product Insights) adds product-level breakdown by top revenue products, impact of discount rate on profit, sales by ship mode, and sales by customer segment. Both pages include slicers for Segment, Order Year, Region, Ship Mode, and Category, making every chart interactive.

---

## Key Findings

### Category Performance

Technology is the most profitable category at \$70,158 (53% of total profit) on \$370,000 in revenue, implying a 19% net profit margin. Office Supplies generates \$54,789 (41% of total profit) on \$370,000 in revenue at a 15% margin. Furniture produces only \$7,569 (6% of total profit) on \$380,000 in revenue, the highest revenue category with the lowest profit, at just a 2% margin.

Furniture is the most urgent problem in the category mix. It generates the most revenue and the least profit. The combination of high discounting in the Furniture category and the structural losses in Tables and Bookcases explain most of this.

### Sub-Category Profitability

The five most profitable sub-categories are Technology items: Copiers (\$22,403), Phones (\$20,939), and Accessories (\$19,209) account for the top three positions. Paper (\$16,285) and Chairs (\$13,201) round out the top five.

Two sub-categories are loss-making: Tables at (\$10,997) loss and Bookcases at (\$1,247) loss. Supplies is marginally negative at (\$754) loss.

Tables is the single most damaging sub-category in the catalogue. It generates revenue but destroys value. The consistent discounting pattern visible in the Discount analysis confirms that Tables is being sold at a loss to move inventory, and the loss is large enough to offset the profitability of several other sub-categories entirely.

### Regional Performance

West leads by sales volume at \$332,444, closely followed by East at \$330,695. Central generates \$246,315 and South generates \$190,409. California is the top-performing state at \$0.21M in sales, followed by New York at \$0.15M and Texas at \$0.08M.

The West and East together generate 60% of total revenue. Any growth strategy that concentrates marketing and fulfilment investment in these two regions will have the highest marginal return.

### Customer Segment Analysis

Consumer segment is the largest at \$558,251 (51% of total revenue). Corporate accounts for \$342,603 (31%). Home Office contributes \$199,009 (18%).

The Consumer segment dominates volume but the Corporate segment tends to place larger individual orders and is less likely to apply discount codes. A targeted Corporate sales effort that grows the Corporate share from 31% to 40% without increasing discounting would meaningfully improve the overall profit margin.

### Shipping Mode

Standard Class handles 58.66% of all orders (volume: ₦645K in sales) and generates the most profit at \$77,783. Second Class accounts for 20.19% of orders (\$222K in sales, \$26,925 profit). First Class handles 15.43% (\$170K in sales, \$25,887 profit). Same Day handles 5.73% of orders (\$63K in sales, \$1,921 profit).

Same Day shipping generates the lowest profit despite being the most expensive shipping mode for the business to provide. The volume is small enough that this is not a critical issue, but it suggests that Same Day pricing may not be recovering the full cost of the service.

### Discount Impact on Profit

This is the most important finding in the dataset. Orders with zero discount generate \$149,265 in profit, which is 113% of the reported total profit. This means that the discounting strategy, taken in aggregate, is destroying \$16,749 of profit that the business would otherwise keep.

The tipping point is between 20% and 30% discount. At 20% discount, the profit contribution is still positive at \$45,534. At 30% discount, orders turn loss-making at (\$5,130) aggregate loss. Every discount band above 30% produces a net loss, with the 80% discount band producing the largest individual loss at (\$20,018).

The business is profitable despite its discount strategy, not because of it.

---

## Recommendations

**Retire or reprice Tables and Bookcases.** Tables is losing \$10,997 on revenue that appears healthy on the surface. The loss is systematic, not seasonal, and the discount analysis confirms that Tables items are being discounted at rates above 30% regularly. Discontinue the highest-discount SKUs within Tables or reprice to cover costs. Bookcases can be retained but should not be discounted above 15%.

**Cap discounts at 20% across all categories.** The data is unambiguous: 20% discount is the last point at which the business remains profitable at the aggregate level. Every band above 20% produces a net loss. A discount policy that caps promotional rates at 20% and requires Finance sign-off for any exception would recover an estimated \$16,749 per equivalent sales cycle — essentially recovering an additional 12.6% on total profit.

**Prioritise Corporate segment growth.** Corporate customers at \$342K revenue and higher average order values without consumer-level promotional sensitivity represent the best growth opportunity. A dedicated Corporate account management programme targeting the East and West regions (the two highest-revenue areas) does not require a discounting strategy to win business.

**Invest in the West and East.** With 60% of revenue coming from these two regions and California and New York as the clear leaders, any investment in marketing, fulfilment speed, or account management in these markets has the highest expected return per dollar spent.

**Review Same Day shipping economics.** At 5.73% of orders and the lowest profit contribution of any shipping mode, the current pricing of Same Day service may not be recovering its cost. A cost analysis of the fulfilment model for Same Day orders would confirm whether this service should be repriced or restricted to high-AOV orders only.

---

## Dashboard Screenshots

**Page 1: Executive Sales Overview**

Revenue of \$1.10M, Profit of \$132.52K, Quantity 19K, Orders 5K. Visualisations: Top Performing States by Sales (bar chart), Profit by Sub-Category (horizontal bar, Tables highlighted in orange as the only loss-maker shown), Monthly Sales Trend 2014 to 2017 (line chart showing consistent year-on-year growth), Sales by Category (bar chart, Technology and Furniture nearly equal in revenue, Office Supplies slightly behind).

**Page 2: Business Intelligence Performance and Customer Insights**

Slicers for Segment, Order Year, Region, Ship Mode, and Category. Visualisations: Sales by Product Name (top 10 products by revenue, Canon imageCLASS leads), Impact of Discount on Profit (scatter plot by category showing the clear profit destruction at high discount rates), Sales by Ship Mode (donut chart, Standard Class dominates at 58.66%), Sales by Segment (treemap, Consumer the largest block at \$558K, Corporate \$343K, Home Office \$199K).

---

## File Structure

```
superstore-sales-analysis/
├── Superstore_analysis_workbook.xlsx
│   ├── Cleaned_Data          Source data post-cleaning
│   ├── Category              PivotTable by product category
│   ├── Sub-Category          PivotTable by sub-category
│   ├── Region                PivotTable by region
│   ├── Segment               PivotTable by customer segment
│   ├── Discount              PivotTable by discount band
│   ├── Shipping Mode         PivotTable by ship mode
│   ├── Time Series           Monthly sales by year
│   ├── Total Orders          Order count summary
│   └── Dashboard             Combined summary sheet
├── screenshots/
│   └── screenshot.png        Power BI dashboard export
└── README.md
```

---

## About Elizabeth Williams

I am a Data Analyst and Business Analyst based in Lagos, Nigeria, with over five years of professional experience in financial management and accounting. This analysis was built as part of my data analytics portfolio to demonstrate proficiency in Excel-based data preparation, PivotTable analysis, and Power BI dashboard design.

**Contact:** lizzyiwo@gmail.com
**Portfolio:** [lizzyiwo.github.io/ElizabethW_data](https://lizzyiwo.github.io/ElizabethW_data/)
**LinkedIn:** [linkedin.com/in/elizabeth-williams50](https://www.linkedin.com/in/elizabeth-williams50)
**GitHub:** [github.com/lizzyiwo](https://github.com/lizzyiwo)

