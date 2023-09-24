# BUSINESS GROWTH ANALYSIS OF SIMULATED COMPANY: MAVEN FUZZY FACTORY
Maven Fuzzy Factory: SQL-driven business growth analysis project showcasing data analysis skills. This project is intended for personal use.

# Description
This project analysed a fictional online retailer called 'Maven Fuzzy Factory' over a three-year period using a simulated database. The goal was to understand the company's growth and gain practical business insights.

Maven Fuzzy Factory's operations, tracking things like sales, customer behaviour, and finances are explored via meticulous SQL query and analysis. The data revealed trends and patterns that gave insights into the company's market position, customer strategies, revenue, and efficiency.

While Maven Fuzzy Factory is imaginary, this project demonstrates how data analysis can provide real-world insights.


# Table of contents

- [Installation](#installation)
- [Dataset Description](#dataset-description)
- [Analysis](#analysis)
- [Results](#results)
- [Discuss and Decisions](#discuss-and-decisions)
- [Contributing](#contributing)
- [License](#license)

## Installation
1. **Pre-requisites:** Have MySQL Workbench installed.

2. **Prepare the settings:** via [SETUP](https://github.com/vankhanh126/Maven-Fuzzy-Factory/blob/main/SETUP.sql)

3. **Set up the database:** via [DATABASE](https://github.com/vankhanh126/Maven-Fuzzy-Factory/releases/tag/database)


## Dataset Description

The database is a simulated representation and does not contain real data. It contains 6 tables that record orders, products, and websites information of Maven Fuzzy Factory over three years starting from March 2012.



### 1. "orders" table
The table contains essential information about customer orders, hence used to track and analyse the sales and transactions within Maven Fuzzy Factory.

| Column Name          | Description                                           |
|----------------------|-------------------------------------------------------|
| **order_id**         | Unique identifier for each customer order.            |
| **created_at**       | Timestamp indicating when the order was created.     |
| **website_session_id** | Unique identifier for the website session.          |
| **user_id**          | Unique identifier for the customer who placed the order. |
| **primary_product_id** | Identifier of the primary product ordered.         |
| **items_purchased**  | Quantity of the primary product purchased in each order. |
| **price_usd**        | Total order price in US dollars, including product cost and additional charges. |
| **cog_usd**          | Cost of goods (COG) associated with the order in US dollars. |




### 2. "order_items" table
The table provides detailed information about individual items within customer orders, hence used to understand product-level data and order composition.

| Column Name          | Description                                           |
|----------------------|-------------------------------------------------------|
| **order_item_id**    | Unique identifier for each order item.                |
| **created_at**       | Timestamp indicating when the order item was created. |
| **order_id**         | Identifier linking the order item to a specific order. |
| **product_id**       | Identifier for the product associated with the item.  |
| **is_primary_item**  | Indicator of whether the item is the primary product in the order. |
| **price_usd**        | Price of the order item in US dollars.               |
| **cogs_usd**         | Cost of goods (COG) for the order item in US dollars. |




### 3. "order_item_refunds" table
The table contains valuable information about refunds associated with individual order items, hence used to track and analyse refunds, refund amounts, and their impact on the business.

| Column Name              | Description                                           |
|--------------------------|-------------------------------------------------------|
| **order_item_refund_id** | Unique identifier for each order item refund.          |
| **created_at**           | Timestamp indicating when the refund was processed.   |
| **order_item_id**        | Identifier linking the refund to a specific order item. |
| **order_id**             | Identifier of the order associated with the refund.    |
| **refund_amount_usd**    | Amount refunded in US dollars for the order item.     |




### 4. "products" table
The table contains essential information about the products offered by Maven Fuzzy Factory, hence used to manage our product inventory and track product details.

| Column Name   | Description                                       |
|---------------|---------------------------------------------------|
| **product_id** | Unique identifier for each product.              |
| **created_at** | Timestamp indicating when the product was added. |
| **product_name** | Name or description of the product.           |



### 5. "website_pageviews" table
The table captures data related to pageviews on the Maven Fuzzy Factory website, hence used to understand user engagement and website performance.

| Column Name           | Description                                           |
|-----------------------|-------------------------------------------------------|
| **website_pageview_id** | Unique identifier for each website pageview.          |
| **created_at**        | Timestamp indicating when the pageview occurred.     |
| **website_session_id** | Unique identifier for the website session associated with the pageview. |
| **pageview_url**      | URL of the web page that was viewed during the pageview. |




### 6. "website_sessions" table
The table stores information about user sessions on the Maven Fuzzy Factory website, hence used to study user behavior, marketing effectiveness, and device usage.

| Column Name           | Description                                           |
|-----------------------|-------------------------------------------------------|
| **website_session_id** | Unique identifier for each website session.          |
| **created_at**        | Timestamp indicating when the session started.      |
| **user_id**           | Identifier for the user associated with the session. |
| **is_repeat_session** | Indicator of whether the session is a repeat session. |
| **utm_source**        | Source of traffic for the session. |
| **utm_campaign**      | Marketing campaign identifier associated with the session. |
| **utm_content**       | Specific content identifier for the session. |
| **device_type**       | Type of device used for the session (e.g., desktop, mobile). |
| **http_referer**      | HTTP referer URL, indicating the previous page or source of the session. |







