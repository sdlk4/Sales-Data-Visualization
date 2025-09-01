# Power BI Sales Dashboard
Welcome to the Power BI Sales Dashboard Project, an end-to-end guide to building a robust and interactive sales analytics dashboard. This project demonstrates how to transform raw sales data into meaningful insights using Power BI.

# Project Overview
The objective of this dashboard is to analyze and visualize key sales metrics to support data-driven business decisions. 

The report provides insights on:
- Total Sales performance tracking
- Profit and Profit Margin analysis
- Orders Analysis and trends
- Year-over-Year (YoY) Sales Comparison
- Top 5 Cities by Sales performance
- Sales and Profit by Product, Customer, and Channel
- Interactive filtering through slicers (Date, City, Product, Channel)

This project is designed to help organizations identify trends, optimize sales strategies, and improve profitability.

# Features
- Interactive Dashboard → Dynamic visuals with slicers for Date, City, Product, and Channel
- Advanced Analytics → DAX measures for calculating Total Sales, Profit, Profit Margin, YoY comparisons, and growth percentages
- Visual Insights → Sales by Product, Month, Top Cities, Profit by Channel, and Sales by Customer
- Data Modeling → Proper relationships between tables and a Date Table for time intelligence
- Automation → All metrics update automatically with changes in the dataset

# Tools and Technologies
- Power BI Desktop - Main development platform
- Power Query - ETL: Extract, Transform, Load
- DAX - Data Analysis Expressions
- Excel Dataset - Source data
- GitHub - Project repository

# Project Structure
- Power-BI-Sales-Dashboard/
- │
- ├── salesdash.pbix             # Power BI project file
- ├── report.xlsx                # Dataset used for the dashboard
- ├── README.md                  # Project documentation
- └── screenshots/               # Dashboard screenshots (optional)

# Steps to Create the Dashboard
1. Data Collection
- Gather sales data from multiple sources (Excel, databases, etc.)
2. Power Query (ETL)
- Clean and transform data
- Remove duplicates and handle missing values
- Merge tables and create proper data structure
3. Create Date Table
- Required for DAX time intelligence calculations
- Enables year-over-year comparisons
4. Data Modeling
- Define relationships between tables
- Set primary keys and hierarchies
- Optimize model performance
5. Develop Reports
- Create visuals including charts, tables, maps, and cards
- Design intuitive user interface
6. Implement DAX Calculations
- Key DAX measures used in the project:

- DAXSales = SUM(Sales_Data[Sales])
- Sales PY = CALCULATE([Sales], SAMEPERIODLASTYEAR(DateTable[Date]))
- Sales vs PY = [Sales] - [Sales PY]
- Sales vs PY % = DIVIDE([Sales vs PY], [Sales], 0)
- Profit = SUM(Sales_Data[Profit])
- Profit LY = CALCULATE([Profit], SAMEPERIODLASTYEAR(DateTable[Date]))
- Profit vs LY = [Profit] - [Profit LY]
- Profit vs LY % = [Profit vs LY] / [Profit]
- Profit Margin = DIVIDE([Profit], [Sales], 0)

# Key Insights Derived
- Sales Performance: Sales decreased by over 10% in 2019
- Product Analysis: Drop in sales for the top 7 products
- Customer Impact: Four customers contributed to declining sales
- Channel Performance: Export channel shows higher profit margins

# Dashboard Components
Main KPIs
- Total Sales
- Total Profit
- Profit Margin %
- YoY Growth %

# Visual Elements
- Sales trend over time (line chart)
- Top 5 cities by sales (bar chart)
- Sales by product category (pie chart)
- Profit by sales channel (column chart)
- Customer performance table
- Interactive slicers for filtering

# How to Use
- Download Files: git clone https://github.com/sdlk4/Sales-Data-Visualization.git
- Open Power BI File
- Launch Power BI Desktop
- Open salesdash.pbix
- Refresh Data (if needed)
- Ensure report.xlsx is in the correct path
- Click "Refresh" to update data
- Interact with Dashboard
- Use slicers to filter by date, city, product, or channel
- Hover over visuals for detailed tooltips
- Click on charts to cross-filter other visuals

# Key Learning Outcomes
- Power Query: Data cleaning and transformation techniques
- DAX Functions: Time intelligence and calculation measures
- Data Modeling: Creating relationships and hierarchies
- Visualization: Best practices for dashboard design
- Business Intelligence: Converting data into actionable insights

# Contributing
Want to improve this dashboard?
- Fork the repository
- Add new features or visuals
- Optimize DAX calculations
- Submit a pull request

# Future Enhancements
- Integration with real-time data sources
- Advanced forecasting models
- Mobile-optimized dashboard layout
- Automated report distribution
- Additional KPIs and metrics

# Technical Notes
- Dashboard optimized for Power BI Desktop and Power BI Service
- Date table enables proper time intelligence functions
- All measures use best practices for DAX performance
- Data model follows star schema design principles
- Compatible with Power BI Pro and Premium licenses
