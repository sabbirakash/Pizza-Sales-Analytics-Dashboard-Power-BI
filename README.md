# 🍕 Pizza Sales Analytics Dashboard | Power BI

<p align="center">
  <img src="https://github.com/sabbirakash/Pizza-Sales-Analytics-Dashboard-Power-BI/blob/main/Images/Pizza%20Model%20Banner.png">
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
<img src="https://github.com/sabbirakash/Pizza-Sales-Analytics-Dashboard-Power-BI/blob/main/Images/Pizza%20Model%20Dashboard.png" width="100%">
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


---

# 🧮 DAX Measures & KPIs

Several DAX measures were developed to calculate operational KPIs and improve dashboard interactivity.

## 📌 Core KPIs

| Measure | Description |
|---------|-------------|
| **Total Revenue** | Sum of revenue generated from all pizza sales |
| **Total Orders** | Count of distinct order IDs |
| **Total Pizzas Sold** | Sum of all pizza quantities sold |
| **Average Order Value** | Total Revenue divided by Total Orders |
| **Average Pizzas per Order** | Total Pizzas Sold divided by Total Orders |
| **Total Revenue by Category** | Revenue generated by each pizza category |
| **Total Revenue by Size** | Revenue generated by each pizza size |
| **% of Sales by Category** | Percentage contribution of each category |
| **% of Sales by Size** | Percentage contribution of each size |

## 📊 Key Metrics

| Metric | Value |
|--------|-------:|
| Total Revenue | $817,860 |
| Total Orders | 21,350 |
| Total Pizzas Sold | 49,574 |
| Average Order Value | $38.31 |
| Average Pizzas per Order | 2.32 |

These KPIs provide restaurant managers with an instant overview of sales performance and help track business growth.

---

# 📊 Dashboard Features

The dashboard was designed with a strong focus on usability, interactivity, and executive reporting.

### Executive KPI Cards

- Total Revenue
- Total Orders
- Total Pizzas Sold
- Average Order Value
- Average Pizzas per Order

---

### Interactive Visualizations

- **Daily Trend for Total Orders**: Bar chart showing orders by day of the week
- **Monthly Trend for Total Orders**: Line chart showing orders by month
- **% of Sales by Pizza Category**: Donut chart showing category share
- **% of Sales by Pizza Size**: Donut chart showing size share
- **Total Pizzas Sold by Category**: Bar chart by category
- **Top 5 Pizzas by Revenue**: Bar chart
- **Top 5 Pizzas by Quantity**: Bar chart
- **Top 5 Pizzas by Total Orders**: Bar chart
- **Bottom 5 Pizzas by Revenue**: Bar chart
- **Bottom 5 Pizzas by Quantity**: Bar chart
- **Bottom 5 Pizzas by Total Orders**: Bar chart

---

### Interactive Filters

Users can dynamically filter the dashboard by:

- **Date Range**: Filter by specific time periods
- **Pizza Category**: Classic, Supreme, Veggie, Chicken
- **Pizza Size**: S, M, L, XL, XXL

This enables detailed exploration without modifying the underlying dataset.

---

# 📄 Dashboard Pages

The report consists of one comprehensive interactive dashboard designed for sales analysis.

## 1️⃣ Pizza Sales Analytics Dashboard

<p align="center">
<img src="https://github.com/sabbirakash/Pizza-Sales-Analytics-Dashboard-Power-BI/blob/main/Images/Pizza%20Model%20Dashboard.png" width="100%">
</p>

### 🎯 Purpose

This dashboard provides a complete overview of pizza sales performance, enabling restaurant managers to monitor sales trends, analyze customer ordering patterns, and identify best and worst performing products.

### 📈 Key KPIs

- Total Revenue
- Average Order Value
- Total Pizzas Sold
- Total Orders
- Average Pizzas per Order

### 📊 Visualizations Included

- Daily Trend for Total Orders
- Monthly Trend for Total Orders
- % of Sales by Pizza Category
- % of Sales by Pizza Size
- Total Pizzas Sold by Pizza Category
- Top 5 Pizzas by Revenue, Quantity, and Total Orders
- Bottom 5 Pizzas by Revenue, Quantity, and Total Orders

### 💼 Business Value

This page helps decision-makers:
- Monitor overall sales performance
- Identify peak business hours and days
- Optimize menu based on product performance
- Plan inventory and staffing
- Improve pricing and promotional strategies

---

# 📈 Key Business Findings

The dashboard uncovered several important operational insights regarding pizza sales performance.

## 🍕 1. Strong Revenue Performance

The restaurant generated **$817,860** in total revenue from **21,350 orders**, with an average order value of **$38.31**, indicating a healthy business with consistent customer demand.

---

## 📊 2. Category Performance

- **Classic** pizzas contribute the highest sales percentage
- **Supreme** follows as the second most popular category
- **Chicken** and **Veggie** categories contribute lower shares

**Key Insight**: Classic pizzas are the backbone of the menu, while Veggie has potential for growth.

---

## 📏 3. Size Distribution

- **Large (L)** pizzas account for the highest percentage of sales
- **Medium (M)** pizzas follow closely
- **Small (S)** pizzas contribute a moderate share
- **XL and XXL** sizes contribute minimal sales

**Key Insight**: Large and Medium sizes dominate customer preferences, suggesting menu focus on these sizes.

---

## 📅 4. Daily Order Trends

- **Friday** and **Saturday** show the highest order volumes
- **Sunday** through **Thursday** show moderate but consistent order patterns

**Key Insight**: Weekends are the busiest periods, requiring additional staffing and inventory.

---

## 🕐 5. Hourly Order Patterns

- Peak order hours are **12:00 PM – 1:00 PM** (lunch) and **5:00 PM – 8:00 PM** (dinner)
- Lowest order volumes occur during early morning and late night hours

**Key Insight**: Lunch and dinner rush hours require optimized kitchen and delivery operations.

---

## 📈 6. Monthly Sales Trends

- Highest orders recorded in **July** and **May**
- Lowest orders recorded in **September** and **December**
- Seasonal fluctuations suggest demand patterns linked to holidays and weather

**Key Insight**: Sales peak during summer months, presenting opportunities for targeted promotions.

---

## 🏆 7. Top Performing Pizzas

**By Revenue:**
- The Thai Chicken Pizza
- The Barbecue Chicken Pizza
- The California Chicken Pizza
- The Classic Deluxe Pizza
- The Spicy Italian Pizza

**By Quantity:**
- The Classic Deluxe Pizza
- The Barbecue Chicken Pizza
- The Hawaiian Pizza
- The Pepperoni Pizza
- The Thai Chicken Pizza

**By Orders:**
- The Classic Deluxe Pizza
- The Barbecue Chicken Pizza
- The Hawaiian Pizza
- The Pepperoni Pizza
- The Thai Chicken Pizza

**Key Insight**: Chicken-based and Classic pizzas dominate the top performers.

---

## 📉 8. Worst Performing Pizzas

**By Revenue:**
- The Brie Carre Pizza
- The Mediterranean Pizza
- The Calabrese Pizza
- The Spinach Supreme Pizza
- The Soppressata Pizza

**By Quantity:**
- The Brie Carre Pizza
- The Mediterranean Pizza
- The Calabrese Pizza
- The Spinach Supreme Pizza
- The Soppressata Pizza

**By Orders:**
- The Brie Carre Pizza
- The Mediterranean Pizza
- The Calabrese Pizza
- The Spinach Supreme Pizza
- The Soppressata Pizza

**Key Insight**: These pizzas contribute minimal revenue and could be considered for removal or repositioning.

---

## 📉 9. Low Average Pizzas per Order

The average pizzas per order is **2.32**, indicating that most customers order 2-3 pizzas per transaction.

**Key Insight**: Opportunity to increase average order size through combo offers and upselling.

---

# 🚀 Recommendations

Based on the dashboard analysis, several operational improvements can help enhance sales performance and customer satisfaction.

## 1️⃣ Optimize Menu Based on Performance

- **Promote** top performers: Thai Chicken, Barbecue Chicken, Classic Deluxe
- **Re-evaluate** bottom performers: Brie Carre, Mediterranean, Calabrese
- Consider removing or redesigning low-performing pizzas

---

## 2️⃣ Focus on Large and Medium Sizes

- Since L and M sizes dominate sales, ensure adequate inventory and ingredients for these sizes
- Consider introducing combo deals for L and M pizzas

---

## 3️⃣ Leverage Peak Hours

- Increase staffing during lunch (12-1 PM) and dinner (5-8 PM) rush hours
- Optimize delivery operations during peak periods
- Introduce happy hour promotions during off-peak hours

---

## 4️⃣ Weekend Promotions

- Since Friday and Saturday are busiest, run weekend specials
- Consider family combo offers for weekends
- Ensure sufficient inventory for weekend demand

---

## 5️⃣ Summer Campaigns

- Sales peak in May and July — launch summer promotions
- Introduce seasonal pizzas during high-demand months
- Plan marketing campaigns around summer holidays

---

## 6️⃣ Increase Average Order Value

- Introduce combo meals (pizza + drink + side)
- Offer discounts on orders above a certain value
- Implement upselling strategies at checkout

---

## 7️⃣ Optimize Low-Performing Categories

- **Veggie** category has growth potential — introduce new veggie options
- Run targeted promotions for underperforming categories
- Gather customer feedback on low-rated pizzas

---

## 8️⃣ Data-Driven Inventory Management

- Use historical sales data to forecast demand
- Stock ingredients for top-selling pizzas
- Reduce waste by optimizing quantities for low-demand items

---

# 🛠 Skills Demonstrated

## Business Intelligence
- Interactive Dashboard Design
- Executive Reporting
- KPI Development
- Data Storytelling
- Business Analysis

## Power BI
- Power Query
- DAX (Advanced Measures)
- Data Modeling
- Relationships
- Custom Measures
- Dynamic Slicers
- Multi-table Relationships
- Interactive Reporting

## Data Analysis
- Sales Analytics
- Product Performance Analysis
- Customer Behavior Analysis
- Time-Based Trend Analysis
- Revenue Analysis
- Menu Optimization

## Data Visualization
- KPI Cards
- Donut Charts
- Bar Charts
- Line Charts
- Tables
- Interactive Filters

---

# 📂 Repository Structure

```text
Pizza-Sales-Analytics-Power-BI-Dashboard-Project/
│
├── Dashboard/
│   └── Pizza Sales Analytics Dashboard.pbix
│
├── Dataset/
│   ├── orders.csv
│   ├── order_details.csv
│   ├── pizzas.csv
│   └── pizza_types.csv
│
├── Images/
│   ├── Pizza Sales Analytics Banner.png
│   ├── Main Dashboard.png
│   ├── Best Worst Sellers.png
│   └── Dashboard Preview.png
│
├── Documents/
│   ├── Dashboard Requirements.pdf
│   ├── Dashboard Summary.pdf
│   └── DAX & KPI Measures.pdf
│
└── README.md
```

## 🎯 Future Improvements
Potential enhancements for future versions of the dashboard include:

* Real-time data integration with POS systems

* Predictive models for sales forecasting

* Customer segmentation analysis

* Delivery time analysis

* Profit margin analysis by pizza type

* Ingredient cost optimization

* Mobile-optimized dashboard layout

* Row-Level Security (RLS) for role-based access

* Integration with online ordering platforms

* Advanced drill-through capabilities for order-level details

## 📝 Conclusion
The Pizza Sales Analytics Dashboard demonstrates how Business Intelligence can transform raw sales data into actionable operational insights. By combining interactive visualizations, KPI monitoring, category and size analysis, and top/bottom performer analysis, the dashboard provides restaurant managers with a comprehensive view of sales performance.

The analysis highlights significant opportunities to optimize the menu, improve pricing strategies, increase average order value, and better allocate resources across peak periods. Through dynamic filtering and interactive reporting, stakeholders can quickly explore trends, identify best-selling products, and support data-driven decisions that enhance business growth and customer satisfaction.

## 👨‍💻 Author
SABBIR UDDIN AKASH

Data Analyst | Business Intelligence Developer

Connect with me

### 🌐 Portfolio

[Sabbir Uddin Akash](https://sabbirakash.github.io/)

### 💻 GitHub

[Sabbir Akash](https://github.com/sabbirakash)

### 🔗 LinkedIn

[Sabbir Uddin Akash](https://www.linkedin.com/in/sabbirakash/)


If you found this project helpful or interesting, consider giving it a ⭐ to support my work.


## 📄 Disclaimer
This project uses simulated/anonymized pizza sales data for demonstration purposes. The insights and recommendations are based on the analysis of this dataset and should be validated with real business professionals before implementation.
