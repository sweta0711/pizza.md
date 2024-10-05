# pizza.md
# Pizza Sales Data Analysis

This project demonstrates proficiency in using SQL and Power BI to analyze and visualize sales data effectively for a pizza restaurant. The goal of the analysis is to uncover actionable insights into customer preferences, sales trends, and product performance, which can help optimize the restaurant's sales and marketing strategies to increase revenue and customer satisfaction.

## Problem Statement

A popular pizza store wants to optimize its sales and marketing strategies to increase revenue and customer satisfaction. The company needs to analyze its sales data to uncover insights into customer preferences, sales trends, and product performance. The objective is to uncover insights from the data and develop actionable recommendations to drive business growth. The client has divided the problem statement into two sections:

### KPI Requirements
We need to calculate the following metrics to gain insights into our pizza sales performance:
- **Total Revenue**
- **Total Orders**
- **Average Order Value**
- **Total Pizzas Sold**
- **Average Pizzas Per Order**

### Charts Requirements
To visualize various aspects of the pizza sales data and gain insights, we have identified the following chart requirements:
- **Daily trend** for Total Orders
- **Monthly trend** for Total Orders
- **Percentage of sales by pizza Category**
- **Percentage of sales by pizza Size**
- **Total pizzas sold by pizza Category**
- **Top 5 best selling** & **Bottom 5 worst selling pizzas**

## Objectives
Conduct a comprehensive sales performance analysis for a pizza store using SQL queries and visualize the findings using Power BI. The objective is to gain insights into sales trends, revenue distribution, and top-performing products to inform strategic decision-making and optimize sales strategies.

## Deliverables

### 1. SQL Queries:
- Extract and aggregate sales data from the pizza sales dataset to calculate key metrics such as total sales revenue, average order value, and total orders.
- Analyze sales trends over time (hourly, daily, monthly) to identify peak sales periods and seasonal variations.
- Calculate sales performance metrics for individual products, including best-selling pizzas, popular pizza sizes, and revenue contribution by product category.

### 2. Power BI Visualizations:
- Develop interactive dashboards and visualizations to present the analysis findings in a clear and visually appealing manner according to business requirements.
- Create line charts to visualize sales trends over time, with filters for different time periods.
- Generate pie charts to illustrate revenue distribution by product category and size, highlighting top-selling items and revenue contribution.
- Incorporate slicers and filters to allow users to dynamically explore the data and uncover insights based on their specific criteria and interests.

## Software Used
- **MySQL Workbench 8.0**
- **Microsoft Power BI 2024**

## Data Understanding

### 1. Dataset Description
- **Source**: Kaggle
- **Format**: `.csv`
- **Data Span**: January 2015 - December 2015

### 2. Data Structure
There are 4 datasets that contain detailed information about pizza orders, including specifics about pizza variants, quantities, pricing, dates, times, and categorization details.

| Dataset Name   | Rows  | Columns | Description                                                                                      |
|----------------|-------|---------|--------------------------------------------------------------------------------------------------|
| pizzas.csv     | 97    | 4       | Contains unique pizza identifiers, pizza types, sizes, and unit prices.                           |
| pizza_types.csv| 32    | 4       | Contains information on pizza categories, names, and ingredients.                                 |
| orders.csv     | 21,350| 3       | Contains order details, including order ID, date, and time of order.                              |
| order_details.csv | 48,620| 4    | Contains order details, including order IDs, pizza IDs, and quantities.                           |

### 3. Data Quality Assessment
The datasets appear to be relatively clean, with no missing values or obvious data errors. However, further exploration may reveal outliers or inconsistencies that need to be addressed during data cleaning.

### 4. Data Modeling
The data model facilitates a clear understanding of relationships between datasets:

- **pizzas.csv** linked to **pizza_types.csv** through `pizza_type_id`.
- **orders.csv** linked to **order_details.csv** through `order_id`.

### 5. Create Database & Table Structure
- Designed the database schema in MySQL Workbench.
- Imported the four datasets into corresponding tables in the database.

### 6. Crafting Queries
Dividing MySQL queries into three sections:

#### 1. Measure KPIs:
- Total revenue generated from pizza sales.
- Total number of orders placed.
- Average Order Value.
- Total number of pizzas sold.
- Average pizzas per order.
- Total quantity sold from each pizza category.

#### 2. Sales Trend:
- Peak time hours based on total orders.
- Average number of pizzas ordered per day.
- Order trend based on days, months, and quarters.
- Cumulative revenue over time.

#### 3. Product Popularity:
- Category-wise distribution of pizzas.
- Most expensive pizza.
- Top 5 best-selling pizzas based on total orders.
- Top 3 pizzas based on sales for each pizza category.
- Percentage of sales by pizza category.
- Percentage of sales by pizza size.

## Connecting MySQL DB to Power BI
Connected the pizza sales database to Power BI to visualize and analyze the data through interactive dashboards, providing insights to facilitate informed decision-making.

## Data Transformation
In Power Query Editor:
- Merged the four datasets into a unified dataset for easier dashboard creation.
- Transformed abbreviations in the "size" column into descriptive names (e.g., `S` -> `Small`, `M` -> `Medium`, etc.).
- Created a custom column, `Total_price`, by multiplying `quantity` with `unit_price` to calculate the total price for each item.
- Implemented DAX measures to calculate key metrics such as Total Revenue and Average Order Value.

## Building the Dashboard
### 1. KPI Dashboard
Includes:
- Total Revenue, Total Orders, Average Order Value, and Total pizzas sold.
- Busiest days and times, as well as sales performance trends over specific time periods.

### 2. Product Performance Dashboard
Includes:
- Best and worst-selling pizzas through visually engaging charts and tables, providing a comprehensive overview of pizza sales performance.
- Insights into product management strategies and targeted marketing efforts.

![image](https://github.com/user-attachments/assets/a1b89cec-3d1a-49a0-877c-c105b6e3eed9)

![image](https://github.com/user-attachments/assets/919d2730-562d-484b-b56d-b3a8c6821372)



## Insights
- **Fridays, Thursdays, and Saturdays** have the highest sales volume (47% of total weekly sales), while **Sundays and Tuesdays** are slower.
- **Busiest hours** are between 12:00 PM and 1:00 PM, and 5:00 PM to 6:00 PM, indicating high demand during lunch and evening.
- **Peak sales** occur in the second quarter, with **July** being the highest sales month.
- **Large-sized pizzas** represent 46% of total sales, followed by medium (30%) and small (22%).
- Percentage of sales by all pizza categories is relatively equal, with the **Classic** category being the highest.
- **Thai Chicken Pizza** generates the most sales, while **Classic Deluxe Pizza** is the most ordered. The **Brie Carre Pizza** is the least favored.

---

This structure should give a comprehensive yet concise overview of the Pizza Sales Data Analysis project. You can adapt it further based on your specific needs or add visual examples of your dashboard if needed.
