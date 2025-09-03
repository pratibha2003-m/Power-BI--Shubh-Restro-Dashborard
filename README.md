# Power-BI--Shubh-Restro-Dashborard
Power BI project for Shubh Restro – an interactive restaurant dashboard with KPIs, sales insights, top food items, and DAX measures for data-driven decision making.
# 🍽️ Shubh Restro – Power BI Dashboard

## 📌 Project Overview
Designed an **interactive Power BI dashboard** for a restaurant business **(Shubh Restro)** to track and analyze:
- Food item sales and top-performing dishes.
- City/Branch-wise performance.
- Customer orders and revenue trends.
- Profit % and growth insights.

## 🎯 Objectives
- Identify **Top 5 food items by sales**.
- Monitor **daily/weekly/monthly order trends**.
- Track **branch performance** for decision-making.
- Provide KPIs like **Total Sales, Orders, Profit %, Avg Order Value**.

## 🛠️ Tools & Techniques
- **Power BI** (Data Modeling, DAX, Visuals, Filters)
- **Excel** (raw data preparation)
- **DAX Queries** for measures and calculated columns

## 📄 Project Report
👉 [View Full Report (PDF)](./Shubh_Restro_Dashboard.pdf)

## 📸 Dashboard Snapshot
![Dashboard](./README-assets/dashboard-cover.png)

## 🧮 DAX Highlights
See complete list here: [DAX-Measures.md](./DAX-Measures.md)

**Examples:**
```DAX
-- Total Sales
Total Sales = SUMX(Sales, Sales[Quantity] * Sales[Price])

-- Average Order Value
Avg Order Value = DIVIDE([Total Sales], [Total Orders])

-- Top 5 Food Items by Sales
Top 5 Items =
TOPN(
  5,
  SUMMARIZE('Sales', 'Menu'[Item], "Sales", [Total Sales]),
  [Sales], DESC
)
