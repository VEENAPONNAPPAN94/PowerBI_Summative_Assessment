# 📊 Power BI Module End Evaluation

A hands-on Power BI project focused on end-to-end data cleaning, data modeling, visual storytelling, and DAX calculations using an e-commerce sales dataset.

## 🚀 Project Overview
* **Dataset:** `SalesData_1000Rows_WithIssues_copy.csv`
* **Tools Used:** Power BI Desktop, Power Query Editor, DAX (Data Analysis Expressions)

---

## 🛠️ Key Tasks & Implementation

### 1. Data Cleaning & Transformation (Power Query)
* **Missing Values:** Handled nulls and missing records across text, numeric, and date attributes.
* **Duplicates:** Scanned and removed duplicate rows to ensure data integrity.
* **Date Standardization:** Standardized the `OrderDate` column to a clean date format.

### 2. Visualizations & Insights
* **Pie Chart:** Analyzed order distribution across different regions.
* **Column Chart:** Displayed the top 5 trending products based on total order counts using a Top-N filter.
* **Line Chart:** Tracked profit trends over time utilizing Power BI’s built-in date hierarchy.

### 3. DAX Calculations
* **Calculated Table (`EastRegionOrders`):** Filtered records specific to the East region.
```dax
EastRegionOrders = FILTER('SalesData_1000Rows_WithIssues_copy', 'SalesData_1000Rows_WithIssues_copy'[Region] = "East")
Calculated Column (ProfitCostDifference): Computed row-level differences between profit and cost.


ProfitCostDifference = 'SalesData_1000Rows_WithIssues_copy'[Profit] - 'SalesData_1000Rows_WithIssues_copy'[Cost]
Calculated Measure (TotalProfit): Calculated overall aggregate profit.


TotalProfit = SUM('SalesData_1000Rows_WithIssues_copy'[Profit])
