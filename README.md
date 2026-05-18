# 🛒 Retail Sales Dashboard — Tableau Project

> An interactive Tableau dashboard built on a retail dataset, featuring KPI cards, dynamic filters, parameters, and dual-axis charts across two fully connected dashboards.

---

## 📌 Project Overview

This project was developed as part of the **BI Developer Track** at the **ITI (Information Technology Institute)** scholarship program.

It demonstrates real-world data visualization skills using **Tableau Desktop**, connected to a structured retail dataset containing sales, product, customer, and geographic data.

---

## 📊 Dashboards

### 1. Retail Sales Dashboard
The main overview dashboard containing:
- **6 KPI Cards** — Total Orders, Total Quantity Sold, Total Revenue, Total Profit, Average Discount %, Profit Margin %
- **Sales Per Category** — Bar Chart
- **Sales Trend Over Time** — Area Chart with Tooltip Pie (Gender breakdown)
- **Sales by State** — Filled Map
- **Profit Margin % by Region** — Treemap
- **Top 7 Products by Revenue** — Horizontal Bar Chart with Top N Filter

### 2. Deep Analysis Dashboard
An advanced dashboard containing:
- **Dynamic KPI Card** — controlled by KPI Selector Parameter
- **Revenue & Profit by Category** — Dual Axis Chart (Bar + Line)
- **Sales Trend Over Time** — Area Chart
- **Orders & Revenue by Category** — Dual Axis with LOD Expression
- **Product Drilldown** — Category & Product breakdown
- **Orders Distribution by Region** — Donut Chart

---

## ⚙️ Features

| Feature | Description |
|---|---|
| 🔢 KPI Cards | 6 dynamic KPI cards showing key business metrics |
| 🗺️ Map | Filled map showing sales by US state |
| 🍩 Donut Chart | Orders distribution by region using LaDataViz extension |
| 📈 Dual Axis | Revenue & Profit comparison with synchronized axes |
| 🔍 LOD Expression | FIXED LOD to calculate total orders per category |
| 🎛️ Parameters | KPI Selector, Top N, Start Date, End Date, Charts Type |
| 🔎 Filters | Category, Gender, Age Range, Region, Product Name (Wildcard), Measure Filter |
| 🔗 Navigation | Button navigation between the two dashboards |
| 💡 Tooltip | Embedded Pie Chart showing gender sales breakdown on hover |

---

## 🧮 Calculated Fields

| Field | Formula |
|---|---|
| `Total Revenue` | `SUM([Price] * [Quantity])` |
| `Total Profit` | `SUM([Price] * [Quantity]) - SUM([Cost Price] * [Quantity])` |
| `Profit Margin %` | `[Total Profit] / [Total Revenue] * 100` |
| `Average Discount %` | `AVG([Discount])` |
| `Total Orders per Category` | `{ FIXED [Category] : COUNT([Sale ID]) }` |
| `Sales Performance` | IF/THEN classifying sales as High / Medium / Low |
| `Sales Year` | `YEAR([Date])` |
| `Date Filter` | `[Date] >= [Start Date] AND [Date] <= [End Date]` |
| `KPIs` | Dynamic field controlled by KPI Selector Parameter |

---

## 🎛️ Parameters

| Parameter | Type | Purpose |
|---|---|---|
| `KPI Selector` | String List | Switch between KPI metrics dynamically |
| `Top N` | Integer (1–20) | Control number of top products displayed |
| `Start Date` | Date | Filter data from a specific start date |
| `End Date` | Date | Filter data up to a specific end date |
| `Charts` | String List | Switch chart types dynamically |

---

## 🗂️ Dataset

- **File:** `Retail_Data_for_Lab1.xlsx`
- **Source:** ITI BI Developer Track Lab Dataset

| Column | Description |
|---|---|
| Sale ID | Unique order identifier |
| Date | Transaction date |
| Customer ID / Name | Customer information |
| Gender / Age | Customer demographics |
| Region / State / City | Geographic data |
| Category / Product Name | Product classification |
| Price / Cost Price | Revenue and cost data |
| Quantity / Discount | Sales metrics |

---

## 🛠️ Tools Used

- **Tableau Desktop** — Main visualization tool
- **Microsoft Excel** — Data source
- **LaDataViz Extension** — Donut Chart
- **GitHub** — Version control and project hosting

---

## 🚀 How to Run

1. Clone the repository
```bash
git clone https://github.com/yourusername/retail-sales-dashboard.git
```
2. Open Tableau Desktop
3. Open the `.twbx` file
4. The dataset is embedded — no additional setup needed ✅

---

## 👨‍💻 Author

**[اسمك هنا]**
BI Developer Track — ITI Scholarship
📧 [ايميلك هنا]
🔗 [LinkedIn Profile]

---

## 📸 Screenshots

### Retail Sales Dashboard
![Retail Sales Dashboard](screenshots/dashboard1.png)

### Deep Analysis Dashboard
![Deep Analysis Dashboard](screenshots/dashboard2.png)

---

> Built with 💚 as part of the ITI BI Developer Track
