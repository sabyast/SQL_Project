# SQL Project 

This SQL script demonstrates the use of Common Table Expressions (CTEs) to perform complex data manipulations and aggregations on sales data. It calculates the total sales for each product, finds the top 3 best-selling products, calculates the average sales per order, and identifies the orders with the highest sales.

## Table of Contents

- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Data Structure](#data-structure)
- [Usage](#usage)

## Overview

The SQL script uses a series of CTEs to perform the following tasks:

1. `total_sales_per_product`: Calculates the total sales for each product by multiplying the quantity and price and then summing them up for each product.

2. `top_3_products`: Finds the top 3 best-selling products based on their total sales from the `total_sales_per_product` CTE.

3. `average_sales_per_order`: Calculates the average sales per order by summing the total sales for each order.

4. `top_orders`: Finds the orders with the highest sales based on the `order_total` from the `average_sales_per_order` CTE.

Finally, the script uses a final query that joins the `top_3_products` and `top_orders` CTEs to get the details of the top 3 best-selling products and the orders with the highest sales. The results are ordered by total sales and order total in descending order.

## Prerequisites

Before running the SQL script, ensure you have the following:

1. A relational database management system (RDBMS) such as MySQL, PostgreSQL, or SQL Server installed.

2. Access to the RDBMS with necessary permissions to create temporary tables and perform data manipulations.

## Data Structure

The SQL script uses a temporary table called `raw_sales_data` to store the raw sales data. The `raw_sales_data` table has the following columns:

- `order_id`: An integer representing the order identifier.
- `product_id`: An integer representing the product identifier.
- `quantity`: An integer representing the quantity of the product sold in the order.
- `price`: A decimal representing the price of the product.

Sample data has been inserted into the `raw_sales_data` table for demonstration purposes.

## Usage

1. Open your preferred SQL client and connect to your RDBMS.

2. Copy the entire SQL script and paste it into the SQL client.

3. Run the script to execute the series of CTEs and obtain the results of the top 3 best-selling products and the orders with the highest sales.

Please note that this SQL script is just an example, and the complexity can be adjusted by using more extensive data or involving additional joins and calculations based on your specific data requirements.

Feel free to modify the script or the data to test with different scenarios and explore more complex data manipulations using CTEs.
