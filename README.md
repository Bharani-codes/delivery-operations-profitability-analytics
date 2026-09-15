# Delivery Operations & Profitability Analytics

An end-to-end Data Analytics project focused on analyzing delivery operations, operational efficiency, delivery performance, and profitability across a simulated logistics business.

> **Data Disclaimer:** This project uses synthetic data created for learning and portfolio demonstration. It does not represent any real company, customer, or business data.

---

## 📌 Project Overview

The goal of this project is to analyze logistics delivery operations and identify patterns that can help management understand:

- Delivery delays and operational performance
- Warehouse performance
- Delivery partner performance
- Regional delivery trends
- Processing and transit times
- Revenue and profitability
- Loss-making orders
- Customer segment profitability

The project follows an end-to-end analytics workflow:

**Synthetic Data → Snowflake → SQL Cleaning & Transformation → Star Schema → Power BI → DAX → Business Insights**

---

## 🛠️ Technology Stack

- **Python** – Synthetic data generation
- **Snowflake** – Data storage and database
- **SQL** – Data cleaning and transformation
- **Power BI** – Data modeling and visualization
- **DAX** – Measures and analytical calculations
- **GitHub** – Version control and project documentation

---

## 🗂️ Data Model

The Power BI semantic model follows a **Star Schema**.

### Fact Table

**FACT_ORDERS**

Grain: **One row represents one unique customer delivery order.**

Key attributes include:

- Order ID
- Customer ID
- Warehouse ID
- Delivery Partner ID
- Order Date
- Order Dispatched Date
- Promised Delivery Date
- Actual Delivery Date
- Distance
- Order Value
- Freight Cost
- Packaging Cost
- Warehouse Handling Cost
- Delivery Partner Cost
- Order Status

### Dimension Tables

- **DIM_CUSTOMER**
- **DIM_DELIVERY_PARTNER**
- **DIM_WAREHOUSE**
- **DIM_DATE**

---

## 📊 Power BI Dashboard

The dashboard contains three main analytical pages.

### 1. Executive Overview

Provides a high-level summary of the business:

- Total Orders
- Total Revenue
- Total Profit
- Profit Margin
- Loss-Making Orders %
- Late Delivery %
- Monthly Revenue & Profit
- Warehouse delivery performance
- Regional order distribution
- Order status distribution

### 2. Delivery Performance

Focuses on operational performance and delivery delays:

- Average Processing Days
- Average Transit Days
- Late Delivered Orders
- Late Delivery %
- Warehouse performance
- Processing time vs. late delivery
- Delivery partner transit performance
- Regional late-delivery performance
- Dynamic operational analysis

### 3. Warehouse Details

Provides warehouse-level analysis through drill-through:

- Total Orders
- Late Delivery %
- Total Profit
- Loss-Making Orders
- Processing vs. Transit Days
- Order Status Distribution
- Delivery Partner performance
- Customer Segment profitability

---

## ⚙️ Power BI Features Demonstrated

This project demonstrates:

- DAX Measures
- Calculated Columns
- Star Schema Data Modeling
- Interactive Slicers
- Page Navigation
- Drill-through
- Custom Tooltips
- Field Parameters
- Dynamic Metric Switching
- Bookmarks
- Row-Level Security (RLS)
- Cross-filtering and interactions

---

## 🔍 Data Quality & Transformation

The raw dataset intentionally contains realistic data-quality issues to demonstrate an end-to-end data cleaning workflow.

Issues include:

- Duplicate orders
- Missing values
- Inconsistent text formatting
- Invalid delivery dates
- Outlier distance values
- Invalid foreign-key references
- Valid NULL delivery dates for cancelled or failed orders

SQL transformations were used to:

- Standardize categorical values
- Remove duplicate orders
- Handle invalid dates
- Resolve broken foreign-key references
- Add `UNKNOWN` dimension members where required
- Validate referential integrity
- Prepare curated data for Power BI

---

## 💡 Key Business Insights

The analysis identified several notable patterns in the simulated dataset:

1. **West region generated the highest total profit**, supported by its higher order volume.

2. Approximately **89% of orders were successfully delivered**, while the remaining orders were cancelled or failed/returned.

3. **Higher warehouse processing time was associated with higher late-delivery performance** at the warehouse level.

4. **Standard customer orders had the highest loss-making order rate**, followed by Premium and Business segments.

5. **September recorded the highest monthly profit** during the analyzed period.

6. Regional late-delivery rates were relatively close to each other, indicating that delivery delays were not isolated to a single region.

> These findings represent associations observed in the simulated dataset and should not be interpreted as proven causal relationships.

---

## 📁 Repository Structure

```text
delivery-operations-profitability-analytics/
│
├── README.md
├── .gitignore
│
├── Dashboard/
│   └── Delivery_Operations_Analytics.pbix
│
├── data/
│   ├── fact_orders_raw.csv
│   ├── dim_customer_raw.csv
│   ├── dim_delivery_partner_raw.csv
│   ├── dim_warehouse_raw.csv
│   └── dim_date.csv
│
└── docs/
    ├── Delivery_Operations_Profitability_Analytics_Report.pdf
    ├── Delivery_Operations_User_Guide.pptx
    └── Delivery_Operations_Data_Architect_Document.docx
```
## 📚 Project Documentation
Project Report

Detailed documentation covering:

Business problem
Data architecture
Data model
SQL data cleaning
DAX calculations
Power BI dashboard
Business findings
Recommendations
Limitations
Validation
User Guide

Provides instructions for interacting with the Power BI dashboard, including:

Page navigation
Slicers
Bookmarks
Drill-through
Custom tooltips
Row-Level Security
Data Architect Document

Technical documentation covering:

Data architecture
Snowflake implementation
Raw and curated data layers
Star schema
SQL transformation logic
Power BI semantic model
DAX layer
Security
Validation
Deployment considerations
## ⚠️ Limitations
The dataset is synthetic and created for portfolio demonstration.
The analysis identifies associations rather than proving causation.
Fixed and overhead operating costs are not allocated at order level.
The dataset does not contain explicit delay-reason fields.
Results should not be interpreted as actual logistics company performance.
## 🚀 Future Enhancements

Potential improvements include:

Real-time delivery tracking
GPS-based route analysis
Traffic and weather data integration
Predictive late-delivery modeling
Automated anomaly detection
Dynamic cost allocation
Production cloud deployment
## 👤 Author

Bharani Dharan K

B.Tech – Computer and Communication Engineering

Areas of Interest:
Data Analytics | Business Intelligence | SQL | Power BI | Python | AI/ML


**Use this version as-is.** It is written for a portfolio/recruiter audience rather than as a tutorial, and it accurately describes the project as synthetic.
