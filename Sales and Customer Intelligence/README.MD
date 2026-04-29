#  Sales Analytics Dashboard (Power BI)

##  Project Overview

This project is a **complete end-to-end Business Intelligence solution** built using **Power BI**, focusing on **Sales Performance, Product Insights, and Customer Behavior Analysis**.

The dashboard is designed with a **multi-page architecture**, enabling users to explore data at different levels — from high-level KPIs to detailed product drillthrough analysis.

 Detailed Documentation: 

---

##  Dashboard Preview

###  Main Dashboard

<p align="center">
  <img src="DashboardSS.png" width="900"/>
</p>

###  Product Deep Dive

<p align="center">
  <img src="DashboardSS.png" width="900"/>
</p>

###  Customer Analysis

<p align="center">
  <img src="DashboardSS.png" width="900"/>
</p>

###  Drillthrough Page

<p align="center">
  <img src="DashboardSS.png" width="900"/>
</p>

---

##  Business Objectives

* Monitor **Revenue, Profit, Orders, and Return Rate**
* Identify **top-performing products, categories, and regions**
* Analyze **customer segments and return behavior**
* Track **time-based trends (MoM, YoY, YTD)**
* Enable **deep-dive analysis using drillthrough**

---

##  Data Model (Star Schema)

The model follows a **star schema design** for optimal performance:

###  Fact Tables

* `Sales_Fact` → Sales transactions (Revenue, Units, Orders)
* `Returns_Fact` → Return details

###  Dimension Tables

* `Customer_Dim` → Customer details (Segment, Region)
* `Product_Dim` → Product hierarchy (Category, SubCategory)
* `Date_Dim` → Time intelligence (Year, Month)
* `Region_Dim` → Regional mapping

✔ Relationships: Many-to-One
✔ Optimized for **fast filtering and aggregation**

---

##  Dashboard Structure (4 Pages)

---

###  Page 1 — Executive Overview (Main Dashboard)

**Purpose:** High-level business monitoring

####  KPIs

* Total Revenue → **844K**
* Total Profit → **10.14K**
* Total Orders → **1K**
* Return Rate → **5%**

####  Visuals

*  Monthly Revenue Trend
*  Revenue by Segment
*  Top Products by Revenue
*  Revenue by Region

####  Filters

* Year / Quarter / Month
* Segment
* Category

---

###  Page 2 — Product & Category Deep Dive

**Purpose:** Product performance analysis

####  KPIs

* Revenue
* Profit Margin %
* Total Units Sold

####  Insights

* Category × SubCategory performance (Matrix with conditional formatting)
* Top-performing products
* Revenue distribution by category
* Seasonal performance analysis

---

###  Page 3 — Customer & Returns Analysis

**Purpose:** Customer behavior + return analysis

####  KPIs

* Total Customers
* Avg Order Value
* Total Returns
* Return Rate

####  Insights

* Top customers by revenue
* Returns by region
* Segment vs Region performance matrix

---

###  Page 4 — Product Detail (Drillthrough)

**Purpose:** Deep analysis for selected product

####  Features

* Drillthrough enabled using `ProductName`
* Dynamic filtering across all visuals

####  Visuals

* KPI Cards (Revenue, Units, Profit, Returns, Top Region)
* Monthly Sales Trend
* Customer-level purchase table
* Region-wise revenue distribution

✔ Enables **granular decision-making**

---

##  Key KPIs & DAX Highlights

###  Core Measures

```DAX
Total Revenue = SUM(Sales_Fact[TotalAmount])
Total Profit = SUMX(...)
Total Orders = COUNTROWS(Sales_Fact)
Return Rate = DIVIDE([Total Returns], [Total Orders])
```

###  Time Intelligence

```DAX
Revenue MOM % = DIVIDE([Revenue MOM Change], [Revenue Prev Month])
Revenue YOY % = DIVIDE([Revenue YOY Change], [Revenue Prev Year])
Revenue YTD = TOTALYTD([Total Revenue], Date_Dim[Date])
```

###  Advanced DAX

* `CALCULATE()` → context modification
* `FILTER()` → conditional filtering
* `ALL()` → remove filters for % calculations
* `SUMX()`, `AVERAGEX()` → row-level calculations
* `SWITCH()` → KPI classification

---

##  Key Insights Derived

*  **South & North regions** drive majority revenue
*  A few products contribute significantly (Pareto effect)
*  Negative profit in some categories indicates pricing issues
*  Return rate (~5%) highlights operational improvement scope
*  Small customer group generates high revenue (top 10 customers)

---

##  Features & Enhancements

* ✔ Interactive slicers for dynamic filtering
* ✔ Drillthrough navigation for deep analysis
* ✔ Conditional formatting for performance highlighting
* ✔ Clean UI with consistent theme
* ✔ Bookmark-based navigation

---

##  Row-Level Security (RLS)

Implemented region-based access:

```DAX
[RegionName] = "North"
```

✔ Ensures users only see their assigned region data

---

##  Tools & Technologies

* **Power BI Desktop**
* **DAX (Data Analysis Expressions)**
* **Power Query**
* **Star Schema Data Modeling**

---

##  Business Value

This dashboard enables:

*  Data-driven decision-making
*  Performance monitoring across dimensions
*  Deep insights into products & customers
*  Faster analysis with interactive visuals

---

##  Conclusion

This project demonstrates:

✔ Strong understanding of **data modeling**
✔ Advanced **DAX and time intelligence**
✔ Ability to build **interactive dashboards**
✔ Focus on **business insights, not just visuals**

---
