# sales-mis-dashboard-excel
Sales MIS Dashboard using Excel (MIS Executive Project)

# Sales MIS Dashboard – Excel Project

## Project Overview
This project demonstrates a complete Sales MIS reporting system built using Microsoft Excel,
based on the Superstore sales dataset.

## Files
- **Sales_MIS_Dashboard.xlsx** – the finished workbook. Open this.
  - `Dashboard` – KPI cards, Region/Year filter dropdowns, and three live charts
    (Monthly Sales Trend, Category-wise Sales & Profit, Region-wise Sales Contribution).
  - `Data` – the full, cleaned dataset as a structured Excel Table (`SalesData`).
  - `Reports` – pivot-style summaries (Monthly Sales MIS, Region/Category/Segment/Sub-Category
    performance), all driven by live SUMIFS/SUMPRODUCT formulas so they recalculate automatically
    if the underlying data changes.
- **MIS_Sales_Project.csv** – original raw source data (kept for reference).
- **MIS_Sales_Project_Clean.csv** – cleaned version of the source data (see Data Corrections below).
- **Sales_MIS_Dashboard_Divyam_Mahant.pptx** – presentation walkthrough of the dashboard design.

## Objective
- Track monthly sales, profit, and quantity
- Analyze region, category, and segment performance
- Support management decision-making using MIS reports

## Tools Used
- Microsoft Excel
- Formula-driven pivot-style summaries (SUMIFS / SUMPRODUCT) & native Excel Charts
- Data validation dropdowns as Region/Year filters

## Key Reports
- Monthly Sales MIS (chronological, grouped by year)
- Region-wise Sales Contribution
- Category-wise Performance
- Segment-wise Performance
- Sub-Category-wise Performance

## Dashboard Features
- KPI cards (Total Sales, Total Profit, Total Quantity, Profit Margin, Line Items)
- Monthly sales trend chart
- Region & Order Year filter dropdowns that drive the KPI cards and charts
- Management-ready layout

## Data Corrections Made
The original CSV had a few issues that are fixed in `MIS_Sales_Project_Clean.csv` and in the
`Data` sheet of the workbook:
1. **Encoding** – the file was saved as Windows-1252, not UTF-8, which broke standard CSV readers.
2. **Corrupted text** – 225 Product Name values contained stray non-breaking-space characters.
3. **Zip codes** – 449 US postal codes had lost their leading zero (e.g. `6824` instead of `06824`)
   because they were stored as plain numbers; they're now zero-padded and stored as text.
4. **Month ordering bug** – the original dashboard grouped months alphabetically
   (Apr, Aug, Dec, Feb, Jan…) because it grouped on the text "Order Month" field instead of the
   real date. The Monthly Sales MIS report now groups chronologically (Jan → Dec) off the actual
   `Order Date`.

## Author
Divyam Mahant
