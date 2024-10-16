# Powerbi-Assignment

# Power BI Projects - Superstore & Finance Dataset

This repository contains Power BI project solutions to several tasks related to data visualization, DAX calculations, and data modeling. The dataset used for these tasks includes **Superstore Dataset** and **Finance Dataset**. Below is the breakdown of each task, the steps taken, and the approach used.

## Table of Contents
- [Q2: Line and Clustered Column Chart with Growth %](#q2-line-and-clustered-column-chart-with-growth)
- [Q3: Data Modeling - Box Office Data](#q3-data-modeling---box-office-data)
- [Q4: Waterfall Chart for Category-Wise Yearly Analysis](#q4-waterfall-chart-for-category-wise-yearly-analysis)
- [Q5: Hierarchy for Location (Country-State-Region-City-Postal Code)](#q5-hierarchy-for-location)
- [Q6: Bookmarks Based on Date (Year, Quarter, Month)](#q6-bookmarks-based-on-date)
- [Q7: Drill Through for Region-Wise Profit](#q7-drill-through-for-region-wise-profit)
- [Q8: Conditional Formatting](#q8-conditional-formatting)
- [Q9: Finance Dashboard](#q9-finance-dashboard)

---

## Q2: Line and Clustered Column Chart with Growth %

- **Objective**: Compare this year’s sales vs last year’s sales and calculate the growth percentage using DAX.
- **Dataset**: Superstore Dataset
- **Steps**:
  - Imported the Superstore dataset.
  - Created DAX measures for **This Year’s Sales**, **Last Year’s Sales**, and **Growth %**.
  - Visualized the comparison using a **Line and Clustered Column Chart**.
  
- **Key Measures**:
  ```DAX
  SalesTY = CALCULATE(SUM(Sales[Sales]), YEAR(Sales[Order Date]) = YEAR(TODAY()))
  
  SalesLY = CALCULATE(SUM(Sales[Sales]), YEAR(Sales[Order Date]) = YEAR(TODAY()) - 1)

  Growth% = DIVIDE([SalesTY] - [SalesLY], [SalesLY], 0)
