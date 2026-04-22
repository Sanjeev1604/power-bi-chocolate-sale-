# power-bi-chocolate-sale-
# 🍫 Chocolate Sales Dashboard (Power BI)

## Overview
The **Chocolate Sales Dashboard** is an interactive Power BI report built to analyze sales performance, customer behavior, and profitability across chocolate products, brands, and customer segments.

This dashboard enables stakeholders to monitor KPIs, identify trends, and make data-driven decisions.

---

## 🎯 Objectives
- Track overall **Revenue, Profit, and Customer metrics**
- Analyze **sales by category and brand**
- Understand **customer demographics and loyalty behavior**
- Identify **top-performing products**
- Monitor **monthly revenue trends**

---

## 📊 Key KPIs
| Metric | Value |
|------|------|
| Total Revenue |
| Total Profit | 
| Total Customers |
| Total Orders |
| Loyalty Members |
| Avg Discount |

---

## 📈 Dashboard Features

### 🔹 Revenue Analysis
- Revenue by **Month** (trend visualization)
- Revenue by **Category** (Praline, White, Dark, etc.)
- Revenue by **Brand** (Ferrero, Cadbury, Lindt, Mars, etc.)

### 🔹 Profit Insights
- **Cost vs Profit** comparison by category
- **Top 5 products** by profit contribution

### 🔹 Customer Insights
- Customer distribution by **Gender**
- Customer segmentation by **Loyalty**
- Revenue contribution by **Age Group**

### 🔹 Interactive Filters (Slicers)
- Order Date (range filter)
- Brand
- Gender
- Loyalty Status

---

## 🛠 Tech Stack
- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Data Modeling**
- **Data Visualization**

---

## 🧮 Data Model
The dataset includes:

- `order_id`
- `order_date`
- `product_id`
- `store_id`
- `customer_id`
- `quantity`
- `unit_price`
- `discount`
- `revenue`
- `cost`
- `profit`

---

## ⚙️ Key DAX Measures
```DAX
Total Revenue = SUM(Sales[revenue])

Total Profit = SUM(Sales[profit])

Total Customers = DISTINCTCOUNT(Sales[customer_id])

Total Orders = COUNT(Sales[order_id])

Avg Discount = AVERAGE(Sales[discount])

Loyalty % = 
DIVIDE(
    CALCULATE(COUNT(Sales[customer_id]), Sales[loyalty] = "Yes"),
    COUNT(Sales[customer_id])
)
