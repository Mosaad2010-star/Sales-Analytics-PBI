# 📊 Sales Analytics Dashboard using Power BI

An interactive Power BI dashboard designed to uncover insights from sales data using clear visuals and smart KPIs.

![Dashboard Preview](dashboard-preview.png)

---

## 🧠 Problem Statement

The sales team faced several challenges:
- Unclear visibility of top-performing products.
- No easy way to detect sales trends or seasonality.
- Static Excel reports with limited interactivity.
- Time-consuming reporting process.

These issues slowed down data-driven decision-making and operational agility.

---

## 🎯 Objective

To build an interactive Power BI dashboard that:
- Provides clear metrics like revenue, quantity, and order count.
- Visualizes top products and sales trends over time.
- Enables dynamic filtering by product or time.
- Enhances strategic decision-making through self-service analytics.

---

## 📈 Project Workflow: From Problem to Solution

### 1. 🧾 Data Creation
- A synthetic dataset was generated with **500 sales transactions** and the following columns:
  - `OrderID`
  - `OrderDate`
  - `Product`
  - `Quantity`
  - `TotalAmount`
- Products include: Laptop, Smartphone, Tablet, Monitor, Keyboard, Mouse, Headphones.

### 2. 📥 Data Import in Power BI
- The dataset (`sample_sales_data.xlsx`) was imported.
- Table name: `Sales`.
- Data types were validated and column formatting was adjusted.

### 3. 📊 DAX Measures

```DAX
Total Sales = SUM(Sales[TotalAmount])

Total Quantity = SUM(Sales[Quantity])

Number of Orders = DISTINCTCOUNT(Sales[OrderID])

MonthYear = FORMAT(Sales[OrderDate], "MMM YYYY")

Top Product = 
CALCULATE(
    FIRSTNONBLANK(Sales[Product], 1),
    TOPN(1, VALUES(Sales[Product]), CALCULATE(SUM(Sales[TotalAmount])), DESC)
)

### 4. 🧩 Dashboard Design

Visuals used:

- 📈 **Line Chart**: Sales trend over time.
- 📊 **Bar Chart**: Revenue by product.
- 🥧 **Pie Chart**: Sales distribution by product.
- 🧮 **Cards**: Total sales, total quantity, number of orders.
- 🔍 **Slicers**: Product & OrderDate filters for interactivity.

All visuals support cross-filtering for drill-down analysis.

---

## 💡 Insights Uncovered

- Most profitable products by revenue.
- Sales seasonality and monthly trends.
- Peak order periods and underperforming products.
- Quick comparison of product performance across time.

---


---

## 🛠️ Tools & Technologies Used

- **Power BI Desktop** – Data modeling & visual analytics.
- **DAX (Data Analysis Expressions)** – Custom measures and KPIs.
- **Excel** – Mock data generation.

---

## 🚀 Project Impact

This project illustrates how companies can:

- Automate reporting with zero manual effort.
- Enable real-time sales monitoring.
- Provide strategic insights for sales and marketing teams.
- Transition from static spreadsheets to interactive dashboards.

---

## 📬 Contact

For any suggestions or questions:

**GitHub:** [Mosaad2010-star](https://github.com/Mosaad2010-star)  
**Project Repo:** [Sales-Analytics-PBI](https://github.com/Mosaad2010-star/Sales-Analytics-PBI)

---

