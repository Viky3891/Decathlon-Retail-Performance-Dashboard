# Decathlon Retail Performance Dashboard

An interactive, single-page Power BI dashboard that tracks sales, profitability, order activity and product performance for Decathlon retail, comparing **YTD (through 15 Sep 2026)** with the **same period in 2025 (PYTD)**.

## Dashboard Preview

![Decathlon Dashboard](images/Decathlon_Dashboard.png)

## Business Problem

The retail management team needed one report page to:
- Assess whether revenue and profit are improving against last year
- Identify regional contribution and state-level results
- Compare sports, brands and product types for assortment review
- Examine sales, margin and orders together

## Key KPIs (YTD vs PYTD)

| KPI | YTD | PYTD | YoY |
|---|---|---|---|
| Net Sales | ₹55.26M | ₹47.0M | +17.5% |
| Net Gross Profit | ₹21.72M | ₹18.34M | +18.4% |
| Gross Margin | 39.3% | 39.0% | +0.3 pp |
| Net Units Sold | 46K | 40K | +16.4% |
| Net Orders | 24K | 21K | +16.3% |
| Net AOV | ₹2.67K | ₹2.27K | +17.5% |

## Visuals

- **Monthly Net Sales**: current year vs previous year trend
- **Net Sales YTD by Sport**: ranked bar chart with average line
- **Product Type Performance**: scatter plot of sales vs gross margin with internal benchmark lines
- **Net Sales YTD by Region**: donut chart with contribution %
- **Net Sales YTD by Brand**: ranked bar chart with benchmark line

## Filters

State | Sport | Product Tier | Store Name | Payment Method, plus a **Reset Filters** button.

## Data Model

Star schema:
- `sales`: transaction fact table
- `products`: product dimension (Product Type, Sport, Brand)
- `store`: store dimension (State, Region)
- `Date`: continuous calendar table

All relationships are one-to-many (dimension to fact).

## Key Learnings and Approach

- YTD and PYTD calculated with a fixed reporting cutoff, so slicers do not shift the period
- Margin calculated as total profit / total sales, not an average of row-level margins
- AOV calculated from aggregated sales and distinct orders
- Margin change shown in percentage points (pp), not relative %

## Tools Used

Power BI Desktop, DAX, Power Query, Data Modeling

## Repository Structure

```
├── README.md
├── Decathlon_Power_Bi_Project.pbix
├── Decathlon-Dashboard-Business-Requirements.pdf
└── images/
    └── Decathlon_Dashboard.png
```

## How to Use

1. Download `Decathlon_Power_Bi_Project.pbix`
2. Open it in Power BI Desktop
3. Use the left filter panel to explore the data

## Author

**Vikas Pawar**
🔗 [LinkedIn](https://www.linkedin.com/in/vikas-pawar-in)

Feedback and suggestions are welcome!
