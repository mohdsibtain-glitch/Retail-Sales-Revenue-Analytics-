# Retail-Sales-Revenue-Analytics-
Retail Sales &amp; Revenue Analytics 
# 🛍️ Retail Sales & Revenue Analytics — (SQL, Python, DAX, Power Query (M))

A fully formula-driven Excel dashboard analyzing retail sales performance across stores, regions, and categories. Part of a 3-tool retail analytics portfolio project (SQL + Python + Excel).

## 📁 Workbook Structure

| Sheet | Purpose |
|---|---|
| **Data** | Monthly revenue rolled up by Store × Category — the source table that feeds every formula in the workbook (aggregated from a 66k-row transaction log) |
| **Summary** | SUMIFS/COUNTIFS pivot-style tables: revenue by month, region, category, and store |
| **Dashboard** | KPI cards and charts built on top of the Summary sheet |
| **ReadMe** | In-workbook documentation of sheet structure and data scope |

**Key principle:** nothing is hardcoded. Every cell in Summary/Dashboard is a live formula (`SUMIFS`, `COUNTIFS`, or a direct reference), so the whole workbook recalculates automatically if the Data sheet changes.

## 📊 Data Scope

- **Period:** Jan 2023 – Dec 2024 (24 months)
- **Stores:** 8
- **Regions:** 4 (North, South, East, West)
- **Categories:** 6 (Apparel, Beauty & Personal, Electronics, Grocery, Home & Kitchen, Sports & Fitness)
- **Data grain:** Month × Store × Category, with Units Sold, Order Count, Gross Revenue, Discount Amount, Net Revenue, Total Cost, and Profit per row

## 📈 Headline KPIs

| Metric | Value |
|---|---|
| Total Net Revenue | ₹111,006,121 |
| Total Orders | 66,325 |
| Total Units Sold | 94,128 |
| Avg Order Value | ₹1,673.67 |
| Gross Margin % | 34.0% |

## 🔍 What's Analyzed

- **Net Revenue by Month** — with month-over-month growth %, showing a clear Q4 (Oct–Dec) seasonal spike each year
- **Net Revenue by Region** — North leads (₹34.0M), followed by South (₹25.6M), East (₹24.1M), West (₹27.3M) — margins are consistent (~34%) across all regions
- **Net Revenue & Margin by Category** — Electronics drives the most revenue (₹45.6M) but has the thinnest margin (27.1%); Beauty & Personal has the highest margin (49.4%) despite lower volume
- **Net Revenue by Store** — Downtown Flagship (North) is the top performer at ₹18.7M

## 🛠️ Tech Stack

- Microsoft Excel (or compatible: Google Sheets, LibreOffice Calc)
- Formulas only: `SUMIFS`, `COUNTIFS`, cell references — no VBA, no Power Query, no add-ins required

## 🚀 Getting Started

1. Open `retail_dashboard.xlsx` in Excel or Google Sheets
2. Start on the **ReadMe** tab for an orientation
3. Explore **Data** → **Summary** → **Dashboard** in that order to see how raw rows roll up into KPIs
4. To use your own data: replace the rows in **Data** (keeping the same column headers) — Summary and Dashboard will recalculate automatically

## 🔗 Related Tools in This Portfolio

This Excel workbook is one leg of a 3-part retail analytics project:
- **SQL** — transaction-level analysis (`retail_analytics.db` / `retail_sales.csv`)
- **Python** — deeper statistical/EDA analysis on the same transaction log
- **Excel** (this workbook) — formula-driven executive dashboard

## 📄 License

Feel free to use, modify, and adapt this workbook for your own portfolio.
