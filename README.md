
# Power-BI-sales-report
## 🔍 Overview
This Power BI report provides a visual analysis of **Sales** and **Cost of Goods Sold (COGS)** across different **product families**. It helps stakeholders identify high-performing product categories, assess profitability, and make data-driven decisions.

## 🗂️ Dataset
The report is built using a sample dataset consisting of three main tables:

- `fact sheet`:
  - `Product_id`, `Sales_USD`, `quantity`, `Price_USD`, `COGS_USD`, `Date_Time`, `Account_id`
  
- `accounts`:
  - `Account_id`, `Account`, `country_code`, `Master_id`, `latitude2`, `longitude`, `country2`, `Postal_code`, `street_name`, `Street_number`

- `Dim_product`:
  - `Product_Family`, `Product_Family_Id`, `Product_Group`, `Product_Group_id`, `Product_Name`, `Product_Name_id`, `Product_Size`, `Produt_Type`

## 📊 Key Visuals
- **Stacked Column Chart**: Sales vs COGS by Product Family
- **Card KPIs**: Total Sales, Total COGS, Gross Profit, Profit Margin %
- **Line Chart**: Sales trend over time
- **Bar Chart**: Top 5 Products by Sales
- **Map**: Sales by region/country
- **Slicers**: Filter by Date, Country, Product Family

## 🧮 DAX Calculations Used
- `Total Sales = SUM('fact sheet'[Sales_USD])`
- `Total COGS = SUM('fact sheet'[COGS_USD])`
- `Gross Profit = [Total Sales] - [Total COGS]`
- `Profit Margin % = DIVIDE([Gross Profit], [Total Sales])`
- `YoY Growth % = DIVIDE([Total Sales] - [Sales YoY], [Sales YoY])`

## 📌 Features
- Interactive slicers and filters
- Clean, professional layout
- Smart narrative and executive summary
- Dynamic Top N analysis using DAX

## 💻 How to Use
1. Clone or download the repository.
2. Open the `.pbix` file in Power BI Desktop.
3. Explore the visuals and interact with slicers to customize your view.
4. Modify or extend the DAX formulas to suit your analysis needs.

## 📦 Requirements
- Power BI Desktop (latest version)
