# Power BI Sales Dashboard 

Welcome to the **Power BI Sales Dashboard Project**, an end-to-end guide to building a robust and interactive sales analytics dashboard. This project demonstrates how to transform raw sales data into meaningful insights using Power BI.

## Project Overview

The objective of this dashboard is to analyze and visualize key sales metrics to support data-driven business decisions. The report provides insights on:

- Total Sales
- Profit and Profit Margin
- Orders Analysis
- Year-over-Year (YoY) Sales Comparison
- Top 5 Cities by Sales
- Sales and Profit by Product, Customer, and Channel
- Interactive filtering through slicers (Date, City, Product, Channel)

This project is designed to help organizations identify trends, optimize sales strategies, and improve profitability.

## Features

- **Interactive Dashboard:** Dynamic visuals with slicers for Date, City, Product, and Channel.
- **Advanced Analytics:** DAX measures for calculating Total Sales, Profit, Profit Margin, YoY comparisons, and growth percentages.
- **Visual Insights:** Sales by Product, Month, Top Cities, Profit by Channel, and Sales by Customer.
- **Data Modeling:** Proper relationships between tables and a Date Table for time intelligence.
- **Automation:** All metrics update automatically with changes in the dataset.

## Tools and Technologies

- **Power BI Desktop**
- **Power Query** (ETL: Extract, Transform, Load)
- **DAX** (Data Analysis Expressions)
- **Excel Dataset** (source data)
- **GitHub** (project repository)

## Steps to Create the Dashboard

1. **Gather Data:** Collect sales data from multiple sources (Excel, databases, etc.).
2. **Power Query:** Clean and transform data (remove duplicates, handle missing values, merge tables).
3. **Create Date Table:** Required for DAX time intelligence calculations.
4. **Data Modeling:** Define relationships, primary keys, and hierarchies.
5. **Develop Reports:** Create visuals including charts, tables, maps, and cards.
6. **Implement DAX Calculations:**  
   Example DAX measures:
   -```DAX
   -Sales = SUM(Sales_Data[Sales])
   -Sales PY = CALCULATE([Sales], SAMEPERIODLASTYEAR(DateTable[Date]))
   -Sales vs PY = [Sales] - [Sales PY]
   -Sales vs PY % = DIVIDE([Sales vs PY], [Sales], 0)
   -Profit = SUM(Sales_Data[Profit])
   -Profit LY = CALCULATE([Profit], SAMEPERIODLASTYEAR(DateTable[Date]))
   -Profit vs LY = [Profit] - [Profit LY]
   -Profit vs LY % = [Profit vs LY] / [Profit]
   -Profit Margin = DIVIDE([Profit], [Sales], 0)

## Insights Derived
-Sales decreased by over 10% in 2019.
-Drop in sales for the top 7 products.
-Four customers contributed to declining sales.
-Export channel shows higher profit margins.

## Files in the Repository

-salesdash.pbix – Power BI project file
-report.xlsx – Dataset used for the dashboard

## Conclusion
This project demonstrates the power of Power BI in transforming raw data into actionable insights. Users can interactively explore sales performance, identify growth opportunities, and make informed business decisions.
