# BrewMetrics Coffee Co. BI Project

A version-controlled Power BI solution for analyzing BrewMetrics Coffee Co. sales performance across cities, store formats, products, and time.

## Project Purpose

This project analyzes BrewMetrics Coffee Co. sales data using Power BI. The objective is to build a version-controlled Business Intelligence solution that helps understand overall sales performance, monthly sales changes, product rankings, Cold Brew performance, and differences between cities and store formats.

## Data Model

The Power BI solution uses a star schema consisting of one fact table and four dimension tables.

### Fact Table

- Fact_Sales
  - sale_id
  - date
  - city
  - store_format
  - category
  - item
  - quantity
  - unit_price
  - sales_amount

### Dimension Tables

- Dim_Date
  - date
  - Year
  - Month
  - Month Number
  - Quarter

- Dim_City
  - city

- Dim_Product
  - item
  - category

- Dim_StoreFormat
  - store_format

The dimension tables are connected to Fact_Sales using one-to-many relationships with single-direction filtering.

## DAX Measures

The project includes the following measures:

1. Total Sales
2. MoM Sales Growth %
3. Running Total Sales
4. Product Sales Rank
5. Cold Brew Sales

These measures support monthly growth analysis, cumulative sales analysis, product ranking, and Cold Brew performance analysis.

## Dashboard

The final Power BI dashboard includes:

- Total Sales KPI
- Cold Brew Monthly Sales Trend
- Sales Performance by City
- Sales by City and Store Format
- City Filter slicer
- City to Store Format drill-down

## Key Insights

1. Total sales for the analyzed period are approximately ₹39.66 lakh.

2. Monthly sales increased from April to May by 9.45%, followed by a decline of 16.18% in June. July has a much smaller sales value than the previous months.

3. The city performance chart shows differences in total sales between Bengaluru, Chennai, Hyderabad, and Coimbatore, allowing the business to compare city-level performance.

4. The Cold Brew monthly trend shows strong sales during April and May followed by a decline in June and a sharp reduction in July. This indicates a clear change in Cold Brew sales across the analyzed months.

## Version Control

Git and GitHub are used to maintain the development history of the Power BI solution. The commit history records the project setup, star-schema development, individual DAX measures, and final dashboard development as separate stages.

This project analyzes BrewMetrics Coffee Co. sales data using Power BI. The objective is to build a version-controlled Business Intelligence solution that helps understand overall sales performance, monthly sales changes, product rankings, Cold Brew performance, and differences between cities and store formats.

## Data Model

The Power BI solution uses a star schema consisting of one fact table and four dimension tables.

### Fact Table

- Fact_Sales
  - sale_id
  - date
  - city
  - store_format
  - category
  - item
  - quantity
  - unit_price
  - sales_amount

### Dimension Tables

- Dim_Date
  - date
  - Year
  - Month
  - Month Number
  - Quarter

- Dim_City
  - city

- Dim_Product
  - item
  - category

- Dim_StoreFormat
  - store_format

The dimension tables are connected to Fact_Sales using one-to-many relationships with single-direction filtering.

## DAX Measures

The project includes the following measures:

1. Total Sales
2. MoM Sales Growth %
3. Running Total Sales
4. Product Sales Rank
5. Cold Brew Sales

These measures support monthly growth analysis, cumulative sales analysis, product ranking, and Cold Brew performance analysis.

## Dashboard

The final Power BI dashboard includes:

- Total Sales KPI
- Cold Brew Monthly Sales Trend
- Sales Performance by City
- Sales by City and Store Format
- City Filter slicer
- City to Store Format drill-down

## Key Insights

1. Total sales for the analyzed period are approximately ₹39.66 lakh.

2. Monthly sales increased from April to May by 9.45%, followed by a decline of 16.18% in June. July has a much smaller sales value than the previous months.

3. The city performance chart shows differences in total sales between Bengaluru, Chennai, Hyderabad, and Coimbatore, allowing the business to compare city-level performance.

4. The Cold Brew monthly trend shows strong sales during April and May followed by a decline in June and a sharp reduction in July. This indicates a clear change in Cold Brew sales across the analyzed months.

## Version Control

Git and GitHub are used to maintain the development history of the Power BI solution. The commit history records the project setup, star-schema development, individual DAX measures, and final dashboard development as separate stages.
