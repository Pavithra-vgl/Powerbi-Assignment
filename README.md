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

  ## Q3: Data Modeling - Box Office Data

- **Objective**: Import the 2023 Worldwide Box Office data, merge it with data from the past 3 years, and create a master table in Power Query for further analysis.
- **Dataset**: Box Office Mojo Dataset (2021–2023).
- **Steps**:
  - Imported 2023 Worldwide Box Office data.
  - Added data for the past 3 years (2021–2023) in Power Query.
  - Cleaned and transformed the data, ensuring consistency across the years.
  - Merged the datasets to create a **Master Table** containing box office data for all years.
  - Loaded the **Master Table** into Power BI Desktop for further analysis and visualization.

---

## Q4: Waterfall Chart for Category-Wise Yearly Analysis

- **Objective**: Create a Waterfall chart that provides a category-wise yearly breakdown of performance.
- **Dataset**: Superstore Dataset.
- **Steps**:
  - Imported the Superstore dataset.
  - Prepared the data by categorizing sales and profit information year-wise.
  - Created a **Waterfall Chart** showing a year-on-year performance comparison across different product categories.

---

## Q5: Hierarchy for Location

- **Objective**: Create a hierarchy based on **Country → State → Region → City → Postal Code** and visualize location-wise sales.
- **Dataset**: Superstore Dataset.
- **Steps**:
  - Created a location hierarchy in Power BI consisting of **Country**, **State**, **Region**, **City**, and **Postal Code**.
  - Visualized **Location-wise Sales** using a hierarchical column chart that drills down through the different levels of the location hierarchy.

---

## Q6: Bookmarks Based on Date (Year, Quarter, Month)

- **Objective**: Create bookmarks to filter sales data by **Year**, **Quarter**, and **Month** using the order date field.
- **Dataset**: Finance Dataset.
- **Steps**:
  - Created a **Clustered Column Chart** for sales by order date.
  - Applied **Bookmarks** for Year, Quarter, and Month to dynamically filter the data.
  - Added navigation buttons for each bookmark to enable users to switch between views easily.

---

## Q7: Drill Through for Region-Wise Profit

- **Objective**: Create a Donut Chart showing region-wise profit and implement drill-through functionality for the West Region.
- **Dataset**: Superstore Dataset.
- **Steps**:
  - Created a **Donut Chart** that displays profit by region.
  - Set up a **Drill Through** page specifically for the **West Region** to allow users to explore detailed performance metrics for that region.
  - The drill-through feature provides more in-depth analysis of the West Region's sales and profit.

---

## Q8: Conditional Formatting

- **Objective**: Apply conditional formatting to a table that displays subcategory-wise sales, profit, quantity, and discount data.
- **Dataset**: Superstore Dataset.
- **Steps**:
  - Created a **Table Visual** to show subcategory-wise **Sales**, **Profit**, **Quantity**, and **Discount**.
  - Applied the following conditional formatting:
    - **Sales**: Applied background colors from red (lowest) to green (highest).
    - **Profit**: Added arrow icons, with red for negative profit and green for positive profit.
    - **Quantity**: Applied **Data Bars** to visualize quantity levels.
    - **Discount**: Applied font color formatting, using red for the lowest discounts and green for the highest.

---

## Q9: Finance Dashboard

- **Objective**: Create a **Finance Dashboard** incorporating navigation, cards, charts, website links, and slicers.
- **Dataset**: Finance Dataset.
- **Steps**:
  - Designed a **Dashboard** with key financial metrics displayed using cards, bar charts, and slicers.
  - Added a **navigation bar** for easy filtering based on key metrics such as Year and Profit.
  - Included a link to the company’s website for additional information and context.

---

## How to Use

1. Clone or download the repository.
2. Open the `.pbix` files in **Power BI Desktop** to explore the visualizations and DAX formulas.
3. The solution files are organized by question, making it easy to review the individual tasks.

## Datasets

- **Superstore Dataset**: This dataset includes sales, profit, and regional information.
- **Finance Dataset**: Contains financial data for creating dashboards and visualizations.
- **Box Office Dataset**: Worldwide box office data for data modeling tasks.

---

