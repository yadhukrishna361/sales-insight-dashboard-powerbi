# 📊 Sales Insight Dashboard – Power BI Project

This project demonstrates a **Sales Insight Dashboard** created using Microsoft Power BI. It analyzes multi-dimensional sales data to uncover patterns, trends, and high-value segments. The dashboard serves as a strategic tool for sales and business managers to make data-informed decisions.

## 🎯 Project Objective

The goal of this project was to:
- Consolidate and analyze sales data across markets, products, customers, and time.
- Identify key revenue drivers and top-performing regions.
- Build a dynamic dashboard to assist in decision-making for stakeholders.

## ❓ Key Business Questions

This project aimed to answer the following business questions:
1. Which markets generate the highest revenue and sales volume?
2. What is the monthly/quarterly trend in overall sales revenue?
3. Who are our top 5 customers by revenue contribution?
4. What are our best-performing products?
5. Are there any underperforming areas that require attention?


## 📂 Datasets Used
- <a href="https://github.com/yadhukrishna361/sales-insight-dashboard-powerbi/blob/main/sales_data1.xlsx">Dataset</a>

## ⚙️ Process & Methodology

1. **Data Cleaning**  
   - Used Power Query Editor to remove duplicates, fix null values, and ensure data type consistency.

2. **Data Modeling**  
   - Built a **star schema** with `transactions` as the fact table and others as dimension tables.
   - Defined relationships based on keys (e.g., `CustomerID`, `ProductID`).

3. **Calculated Measures with DAX**  
   - Revenue: `SUM(Transactions[Revenue])`
   - Sales Quantity: `SUM(Transactions[Quantity])`
   - Rank Measures for Top N analysis

4. **Visualizations**  
   - KPI cards, column charts, line chart, bar charts, and slicers for interactivity.
   - Included filters for time, market, and product views.


  ## 📊 Dashboard Features

- **Total Revenue and Sales Qty** KPIs
- **Revenue by Markets** (Bar chart)
- **Sales Qty by Markets** (Bar chart)
- **Revenue Trend Over Time** (Line chart)
- **Top 5 Customers** by revenue (Bar chart)
- **Top 5 Products** (Bar chart)

### 📸 Screenshot:
[Dashboard Screenshot]![sales dashboard](https://github.com/user-attachments/assets/849cb528-b9ec-4c6e-88ae-d751c2541de7)

## 🔍 Insights & Findings

- **Delhi** is the highest revenue-generating market (~520M).
- **Electricalsara Stores** is the top customer contributing over 400M in sales.
- A single unnamed product accounts for nearly 469M revenue (data cleaning opportunity).
- A downward revenue trend was noticed post-2019, needing further investigation.
- Several regions such as **Bangalore** and **Patna** show very low engagement, signaling potential areas for marketing focus.

## ✅ Conclusion

This Power BI dashboard successfully provides a clear picture of sales dynamics across key dimensions. It allows users to drill into specific markets, products, and timeframes, enabling data-driven business strategies. Future improvements could include customer segmentation, forecasting models, or integration with live data sources.

## 🛠️ Tools & Skills Used

- **Power BI Desktop**
- **Power Query Editor**
- **Data Modeling (Star Schema)**
- **DAX (Calculated Measures & KPIs)**
- **Excel/CSV integration**
- **Data Cleaning & Transformation**
- **Business Analysis & Reporting**
