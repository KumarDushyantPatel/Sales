# Sales
Task 3 

In this project, I worked with sales data from year 2015 and 2016 to perform a series of structured data analysis and transformation operations using SQL. 
The steps carried out are outlined below:<br>
**Database and Table Inspection**<br>
Switched to the sales database and retrieved all records from the sales2015 and sales2016 tables.<br>
Described the structure of the sales2015 table to understand its schema.<br>
**Descriptive Analysis**<br>
Calculated the total (SUM) of OrderQuantity from the sales2015 table.<br>
Calculated the average (AVG) of OrderQuantity from the sales2016 table.<br>
**Data Cleaning and Date Formatting**<br>
Identified inconsistencies in the OrderDate format and used the STR_TO_DATE function to standardize dates using two possible formats (%m-%d-%Y and %m/%d/%Y)<br>
Applied a conditional UPDATE query to convert and clean the OrderDate column in the sales2015 table.<br>
Repeated similar steps to clean and standardize the StockDate column in the sales2016 table.<br>
**Window Function Analysis**<br>
Used a FIRST_VALUE() window function partitioned by CustomerKey and ordered by OrderDate to identify the first product purchased by each customer<br>
View Creation for Aggregated Sales<br>
Created a view net_order_sales to compute net sales per order by joining sales2016 with the products table and calculating the total value using OrderQuantity * ProductPrice<br>
**Common Table Expression (CTE) for Subcategory Analysis**<br>
Built a CTE avg_sub_cat_cost to calculate the average product cost by ProductSubcategoryKey.<br>
Joined this CTE with the products table to analyze the cost distribution across different product subcategories.<br>
**Index Creation and Optimization**<br>
Inspected existing indexes in the sales2016 table.<br>
Created a new index idx_sales2016_customer_order on the CustomerKey column to improve query performance for customer-based lookups.<br>
Verified the index creation by displaying all indexes in the table.<br>
