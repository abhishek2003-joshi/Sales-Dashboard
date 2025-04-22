## 📊 Power BI Sales Performance Dashboard
Project Overview
An interactive sales analytics dashboard powered by the AdventureWorks Data Warehouse, designed to monitor team and individual performance across regions, products, and time periods.

Key Features
Interactive Filters: Year, Region, Salesperson

Key Metrics: Lifetime Sales, Year-over-Year (YoY) Growth %, Top Products

Drill-Down Capabilities: Analyze individual performance and regional insights

Product & Region Insights: Focus on top-performing categories and geographies

## 🔧 Technical Implementation
Tools Used
Power BI: Visualization & Dashboard creation

Power Query: ETL (Extract, Transform, Load)

DAX (Data Analysis Expressions): Custom metrics

Data Model
Source: AdventureWorks OLAP Database

Model Type: Star Schema

Fact Tables
FactInternetSales: Online sales transactions

FactResellerSales: B2B sales transactions

FactSalesQuota: Sales targets

Dimension Tables
DimEmployee: Sales team (Names, Regions)

DimProduct: Product details (e.g., Bikes, Clothing)

DimDate: Time hierarchy (Fiscal Year, Month)

DimSalesTerritory: Geographic details (Country, Region)

Star Schema Design
Central Fact Table: FactInternetSales

Linked via keys (e.g., ProductKey, TerritoryKey) to dimension tables

Optimized for fast aggregations and analytics

## ⚙️ ETL Process (Power Query)
Standardized currencies (e.g., ₹ to $)

Cleaned and handled missing values

Added calculated columns such as:

YoY % = DIVIDE([Total Sales] - [Total Sales PY], [Total Sales PY])

YTD Sales = TOTALYTD(SUM(FactInternetSales[SalesAmount]), DimDate[Date])

## 📈 Dashboard Highlights
Team Performance: Filterable table showing regional and annual performance

Individual Growth: Drill-down to view top individual contributions (e.g., Rachel Valdez’s 815% YoY growth)

Product Analysis: Category-wise breakdown showing Bikes as top-selling ($1.38M)
