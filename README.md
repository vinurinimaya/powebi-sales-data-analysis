# Sales-Data-Analysis-Report

### Report Link : <paste your Power BI Service report link here>

## Problem Statement

This report helps the business understand its sales performance. It shows which products drive the most (and least) sales, profit and quantity sold, how sales move over time, how discounts are being used, and where customers are located. By identifying best and worst performers, the business can decide which products to promote, which to review, and where discounting is or isn't paying off.

The report answers the following business requirements:

1. Top / Bottom 5 products by Sales, Profit and Quantity Sold.
2. How sales trends vary over time (daily, monthly, quarterly, annually).
3. The relationship between sales and profit.
4. Comparison of sales, profit and quantity sold between any two periods selected by the user.
5. Average discount offered in each discount (promotion) category.
6. Total number of orders.
7. Order-level details (Sales, Profit, Discount, Net Sales and all remaining fields) that can be filtered using visual filters (Product / Date / Customer / Promotion).
8. Sales by city.

### Steps followed

- Step 1 : Load the sales data into Power BI Services and prepare it in Power Query.
- Step 2 : Build a star-schema data model with one fact table (`Fact Table`) and the dimension tables `Dim Customers`, `Dim Product`, `Dim Promotion`, `Date Table 1` and `Date Table 2`, and create relationships between them.
- Step 3 : Create a separate `Measures Table` to hold all DAX measures (`Sum of Net Sales`, `Total Profit`, `Total Quantity`).
- Step 4 : Create the fact-table date fields `Year`, `Quater` and `Month`, and a date hierarchy (Year > Quarter > Month > Date) for time analysis.
- Step 5 : In the report view, set the page size (1920 x 1080) and apply a theme.
- Step 6 : **Overview page**
  - A card visual shows the total number of orders (distinct count of `OrderID`) - Requirement 6.
  - A line chart `Sales Trend over Time` uses the date hierarchy, so the user can drill between year, quarter, month and day - Requirement 2.
  - A scatter chart `Profit Vs Net Sales` shows the relationship between sales and profit - Requirement 3.
  - A bar chart `Average Discount by Promotion Category` shows the average discount for each promotion category - Requirement 5.
- Step 7 : **Top/Bottom 5 Products page** - Six bar charts (Top 5 and Bottom 5 for each of Net Sales, Profit and Units Sold) by `Product Name`. The ranking is done with visual-level **Top N filters** - Requirement 1.
- Step 8 : **Comparison page** - Two independent date slicers (`Date Filter 1` and `Date Filter 2`, based on `Date Table 1` and `Date Table 2`) drive column charts for Total Sales, Total Profit and Total Quantity Sold, so two periods can be compared side by side - Requirement 4.
- Step 9 : **Table Visual page** - A table lists every order field (`OrderID`, `CustomerID`, `ProductID`, `PromotionID`, Date, Price Per Unit, Units Sold, Total Sales, Discount Percentage, Discount Value, Net Sales, Profit). Slicers for Product Name, Date, Customer Name and Promotion Name filter the table - Requirement 7.
- Step 10 : **Sales by City page** - A map visual plots Net Sales by customer `City` - Requirement 8.
- Step 11 : Titles were added to the visuals and the layout was aligned on each page.

Measures used (paste your DAX here):

        Sum of Net Sales = <your DAX>

        Total Profit = <your DAX>

        Total Quantity = <your DAX>

# Snapshot of report (Power BI Service)

<add screenshot here>

# Report Snapshot (Power BI DESKTOP)

<add one screenshot per page: Overview, Top/Bottom 5 Products, Comparison, Table Visual, Sales by City>

# Insights

A multi-page report (six pages) was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the report (fill in the values from your report);

### [1] Total Number of Orders = <value>

### [2] Top / Bottom 5 Products

    Top 5 by Sales      - <product names>
    Bottom 5 by Sales   - <product names>
    Top 5 by Profit     - <product names>
    Bottom 5 by Profit  - <product names>
    Top 5 by Quantity   - <product names>
    Bottom 5 by Quantity - <product names>

### [3] Sales Trend

    a) Highest sales year / quarter / month - <value>
    b) Lowest sales year / quarter / month  - <value>
    c) Overall trend (increasing / decreasing / seasonal) - <value>

### [4] Sales vs Profit

    <describe the pattern seen in the scatter chart, e.g. whether higher sales lead to higher profit and any outliers>

### [5] Average Discount by Promotion Category

    <promotion name> - <value>
    <promotion name> - <value>

### [6] Sales by City

    Highest sales - <city> (<value>)
    Lowest sales  - <city> (<value>)

### [7] Period Comparison

    Sales, profit and quantity change between the two selected periods change when different dates are selected in the slicers.

Values on the report will change if different visual filters are applied.
