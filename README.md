# 🍕 Pizza Sales Analytics Dashboard | Power BI

<p align="center">
  <img src="https://github.com/yourusername/Pizza-Sales-Analytics-Power-BI-Dashboard-Project/blob/main/Images/Pizza%20Sales%20Analytics%20Banner.png">
</p>

<p align="center">

![Power BI](https://img.shields.io/badge/Power%20BI-Dashboard-F2C811?logo=powerbi&logoColor=black)
![DAX](https://img.shields.io/badge/DAX-Measures-blue)
![Power Query](https://img.shields.io/badge/Power%20Query-Data%20Transformation-success)
![Sales Analytics](https://img.shields.io/badge/Domain-Sales%20Analytics-orange)
![Business Intelligence](https://img.shields.io/badge/Business-Intelligence-yellow)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen)

</p>

---

# 📖 Table of Contents

- [Project Overview](#-project-overview)
- [Business Problem](#-business-problem)
- [Project Objectives](#-project-objectives)
- [Dataset Overview](#-dataset-overview)
- [Dashboard Preview](#-dashboard-preview)
- [Tools & Technologies](#-tools--technologies)
- [Data Cleaning & Preparation](#-data-cleaning--preparation)
- [Data Modeling](#-data-modeling)
- [DAX Measures & KPIs](#-dax-measures--kpis)
- [Dashboard Features](#-dashboard-features)
- [Dashboard Pages](#-dashboard-pages)
- [Key Business Findings](#-key-business-findings)
- [Recommendations](#-recommendations)
- [Conclusion](#-conclusion)

---

# 📌 Project Overview

The restaurant and food delivery industry is one of the most competitive sectors, where understanding customer preferences, sales patterns, and product performance is critical to business success. Pizza restaurants, in particular, face constant pressure to optimize their menu, manage inventory efficiently, and maximize revenue through data-driven decisions.

This project presents an **interactive Pizza Sales Analytics Dashboard** developed in **Microsoft Power BI** to analyze pizza sales data across various pizza types, sizes, categories, and time periods. The dashboard consolidates key performance metrics—including Total Revenue, Total Orders, Total Pizzas Sold, Average Order Value, Average Pizzas per Order, and sales trends by day and hour—into a single reporting solution.

Designed for restaurant managers, sales analysts, and business owners, the dashboard enables users to:
- Monitor overall sales performance
- Identify best-selling and worst-selling pizzas
- Analyze customer ordering patterns by day and hour
- Evaluate category and size-wise sales distribution
- Support data-driven menu optimization and inventory planning

---

# 🚨 Business Problem

Pizza restaurants often face several operational and sales challenges that directly impact revenue and customer satisfaction.

Some of the most common challenges include:

- **Unclear sales trends** — difficulty identifying peak hours and busy days
- **Menu inefficiencies** — lack of visibility into best and worst performing pizzas
- **Inventory mismanagement** — overstocking or stockouts of popular ingredients
- **Pricing optimization** — inability to evaluate revenue contribution by size and category
- **Customer demand patterns** — limited understanding of when customers order most
- **Product portfolio imbalance** — too many low-performing items on the menu
- **Revenue concentration risk** — over-reliance on a few top-selling pizzas

Without an integrated analytical solution, restaurant managers rely on fragmented reports, making it difficult to identify sales opportunities and respond proactively. This dashboard addresses these challenges by providing a centralized, interactive reporting solution that enables stakeholders to monitor sales performance, analyze customer behavior, and make informed operational decisions based on real-time insights.

---

# 🎯 Project Objectives

The primary objective of this project is to transform raw pizza sales data into an interactive Business Intelligence solution that supports operational and strategic decision-making.

The dashboard aims to:

- Analyze total revenue generated across all pizza sales.
- Monitor total orders, total pizzas sold, and average order value.
- Identify best-selling and worst-selling pizzas by revenue, quantity, and orders.
- Track daily and monthly sales trends to identify peak periods.
- Analyze hourly sales patterns to optimize staffing and operations.
- Evaluate sales distribution by pizza category (Classic, Supreme, Veggie, Chicken).
- Evaluate sales distribution by pizza size (S, M, L, XL, XXL).
- Provide percentage contribution of each category and size to total sales.
- Support menu optimization and inventory management decisions.
- Provide detailed insights for management reporting and business growth.

---

# 📂 Dataset Overview

The dashboard is built using a pizza sales dataset containing order-level transaction records for a full year.

### Dataset Summary

| Attribute | Details |
|------------|---------|
| **Domain** | Food & Beverage / Restaurant Sales |
| **Department** | Sales & Operations |
| **Time Period** | Full Year (12 Months) |
| **Total Orders** | 21,350 |
| **Total Pizzas Sold** | 49,574 |
| **Total Revenue** | $817,860 |
| **Dashboard Pages** | 1 Interactive Dashboard |
| **Visualization Tool** | Microsoft Power BI |

### Dataset Files

| File Name | Description |
|-----------|-------------|
| `orders.csv` | Order-level details (order_id, date, time) |
| `order_details.csv` | Line-item details (order_details_id, order_id, pizza_id, quantity) |
| `pizzas.csv` | Pizza master data (pizza_id, pizza_type_id, size, price) |
| `pizza_types.csv` | Pizza type master data (pizza_type_id, name, category, ingredients) |

### Column Descriptions

#### orders.csv
- `order_id` — Unique identifier for each order
- `date` — Date when the order was placed
- `time` — Time when the order was placed

#### order_details.csv
- `order_details_id` — Unique identifier for each line item
- `order_id` — Foreign key linking to orders
- `pizza_id` — Foreign key linking to pizzas
- `quantity` — Number of pizzas ordered in that line item

#### pizzas.csv
- `pizza_id` — Unique identifier for each pizza (e.g., bbq_ckn_s)
- `pizza_type_id` — Foreign key linking to pizza_types
- `size` — Size of the pizza (S, M, L, XL, XXL)
- `price` — Price of the pizza

#### pizza_types.csv
- `pizza_type_id` — Unique identifier for each pizza type
- `name` — Full name of the pizza
- `category` — Category (Classic, Supreme, Veggie, Chicken)
- `ingredients` — List of ingredients used

---

# 📊 Dashboard Preview

## Main Dashboard

<p align="center">
<img src="https://github.com/yourusername/Pizza-Sales-Analytics-Power-BI-Dashboard-Project/blob/main/Images/Main%20Dashboard.png" width="100%">
</p>

## Best/Worst Sellers Analysis

<p align="center">
<img src="https://github.com/yourusername/Pizza-Sales-Analytics-Power-BI-Dashboard-Project/blob/main/Images/Best%20Worst%20Sellers.png" width="100%">
</p>

The dashboard provides a comprehensive view of pizza sales performance, including key revenue metrics, sales trends by day and hour, category-wise distribution, and top/bottom performing pizzas.

---

# 🛠 Tools & Technologies

| Category | Technologies |
|----------|--------------|
| Business Intelligence | Microsoft Power BI |
| Data Transformation | Power Query |
| Data Modeling | Power BI Data Model |
| Calculations | DAX (Data Analysis Expressions) |
| Visualization | Interactive Charts, KPI Cards, Slicers |
| Data Source | CSV Dataset (4 Files) |
| Reporting | Interactive Single-page Dashboard |

---

# 🧹 Data Cleaning & Preparation

Before designing the dashboard, the raw pizza sales dataset was cleaned and transformed using **Power Query** to ensure consistency, improve data quality, and support accurate reporting.

The following data preparation steps were performed:

- Imported all 4 CSV files into Power BI.
- Converted date fields into proper Date data types.
- Converted time fields into proper Time data types.
- Standardized text fields for consistency.
- Verified unique order IDs and pizza IDs.
- Checked for missing and blank values.
- Created a calculated column for **Day Name** from the date field.
- Created a calculated column for **Month Name** from the date field.
- Created a calculated column for **Hour** from the time field.
- Created a calculated column for **Revenue** by multiplying quantity and price.
- Prepared the dataset for efficient data modeling and visualization.

These transformations improved overall data quality and enabled reliable KPI calculations and interactive reporting.

---

# 📊 Data Modeling

A clean and optimized data model was developed to support fast report performance and interactive filtering across the dashboard.

The model consists of:

- **Fact Tables**: `order_details` (line-level sales data)
- **Dimension Tables**: `orders`, `pizzas`, `pizza_types`
- Relationships optimized for filtering and aggregation
- Interactive slicers connected across the report

### Data Model Structure
orders (1) ──── (M) order_details
pizzas (1) ──── (M) order_details
pizza_types (1) ── (M) pizzas
