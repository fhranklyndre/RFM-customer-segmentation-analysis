# RFM Customer Segmentation & Revenue Analysis

## Overview
This project delivers an end-to-end customer and revenue analytics solution designed to help a small business better understand customer behaviour, retention risk, revenue concentration, and product performance using transactional sales data.

Using Google BigQuery, SQL, and Power BI, the analysis transformed raw transactional data into actionable business insights through RFM (Recency, Frequency, Monetary) segmentation, KPI reporting, and interactive dashboard development.

The solution was built to support data-driven decision-making around:
- Customer retention
- Revenue growth
- Product strategy
- Operational reporting
- Customer engagement prioritisation

---

# Business Problem

The business was generating steady sales but lacked visibility into:

- Which customers contributed most to revenue
- Which customers were becoming inactive or disengaged
- Which products drove repeat purchases and customer loyalty
- How revenue was distributed across customer groups
- Where potential revenue leakage existed

As a result, business decisions around customer engagement, retention campaigns, and product focus were largely reactive rather than insight-driven.

---

# Project Objectives

The primary objectives of this analysis were to:

- Segment customers based on purchasing behaviour using RFM analysis  
- Identify high-performing and at-risk customer groups  
- Analyse customer retention patterns and revenue contribution  
- Evaluate product performance across customer segments  
- Build interactive dashboards for business monitoring  
- Support operational and strategic decision-making through KPI reporting  

---

# Dataset Overview

The dataset consisted of transactional sales data containing:

| Column | Description |
|---|---|
| CustomerID | Unique customer identifier |
| OrderID | Unique order identifier |
| OrderDate | Date of transaction |
| ProductType | Product category purchased |
| OrderValue | Revenue generated from transaction |

---

# Tech Stack

| Tool | Purpose |
|---|---|
| Google BigQuery | Data warehousing & SQL transformations |
| SQL | Data modelling & analytical views |
| Power BI | Dashboard development & visualisation |
| DAX | Interactive KPI calculations |
| Power Query | Data transformation |
| Data Modelling | Relationship & slicer management |

---

# Methodology

## 1. Data Consolidation
Monthly transactional datasets were combined into a single unified sales table using SQL UNION operations in BigQuery.

### Example:
```sql
CREATE OR REPLACE TABLE sales_2025 AS
SELECT * FROM sales202501
UNION ALL
SELECT * FROM sales202502;
```

---

## 2. RFM Analysis

Customers were analysed using three behavioural dimensions:

| Metric | Definition |
|---|---|
| Recency | Days since last purchase |
| Frequency | Total number of purchases |
| Monetary | Total revenue generated |

### RFM Scoring
Customers were ranked into deciles using SQL window functions and assigned behavioural scores.

### Customer Segments Created
- Champions
- Loyal VIPs
- Potential Loyalists
- Promising
- Engaged
- Requires Attention
- At Risk
- Lost/Inactive

---

## 3. Analytical SQL Views

Several analytical views were created to support business reporting and dashboard interactivity.

### Key Views Developed

| View Name | Purpose |
|---|---|
| rfm_segments | Customer segmentation |
| segment_summary | Revenue & customer distribution |
| customer_retention_risk | Retention analysis |
| monthly_revenue_trend | Revenue trend monitoring |
| product_performance_by_segment | Product performance analysis |
| revenue_concentration | Revenue dependency analysis |

---

# Power BI Dashboard Development

A 3-page interactive dashboard was developed to support executive reporting and operational analysis.

---

# Dashboard Pages

## 1. Executive Business Summary

### KPIs
- Total Revenue
- Total Customers
- Total Orders
- Average Order Value
- Repeat Purchase Rate

### Insights Provided
- Revenue contribution by customer segment
- Customer distribution across segments
- Monthly revenue trends
- Revenue concentration visibility

---

## 2. Customer Segments & Retention Risk

### KPIs
- Champions Count
- At-Risk Customers
- Revenue at Risk
- Lost/Inactive Customers
- Average Customer Recency

### Insights Provided
- Customer retention risk analysis
- Segment performance comparison
- Behavioural trend analysis
- Revenue exposure visibility

---

## 3. Product & Growth Opportunities

### KPIs
- Best-Selling Product Category
- Top Product Revenue
- Revenue from Top 10% Customers
- Champions Revenue Contribution
- Product Average Order Value

### Insights Provided
- Product revenue trends
- Product performance by customer segment
- Revenue concentration analysis
- Product loyalty patterns

---

# Key Business Insights

## Revenue Concentration
The top 10% of customers contributed approximately **24% of total revenue**, highlighting strong revenue dependency on a relatively small customer group.

## Customer Loyalty
Loyal VIPs generated over **£4K in total revenue**, making them the highest-performing customer segment.

## Retention Risk
“At Risk” and “Requires Attention” customers showed significantly higher recency values and lower purchase frequency patterns, indicating increased churn probability.

## Product Performance
Certain product categories consistently attracted higher-value and repeat customers, indicating stronger product-customer alignment and repeat purchase behaviour.

## Operational Visibility
Interactive dashboards significantly improved visibility into customer behaviour, retention patterns, and product performance trends for business reporting and monitoring.

---

# Recommendations

## Customer Retention
Prioritise targeted retention campaigns for “At Risk” and “Requires Attention” customers to reduce potential revenue leakage exceeding **£1.6K**.

## Product Strategy
Increase focus on products strongly associated with Loyal VIP and Potential Loyalist customer groups to maximise repeat purchases and customer loyalty.

## Customer Engagement
Introduce personalised engagement strategies for lower-frequency customer groups to improve retention and repeat purchase behaviour.

## Revenue Monitoring
Monitor revenue concentration regularly to reduce overdependence on smaller customer cohorts driving overall business revenue.

---

# Data Modelling & Interactivity

To improve dashboard interactivity and cross-page filtering:
- Dimension tables were created
- Relationships were established using a star-schema style model
- Dynamic DAX measures were implemented for KPI responsiveness

This enabled:
- Cross-page slicer functionality
- Dynamic KPI filtering
- Improved dashboard scalability
- Better report interactivity

---

# Challenges Solved

## Challenge
Cross-page slicers were not affecting all visuals due to disconnected summary tables and inconsistent granularity across views.

## Solution
Implemented:
- Dimension tables
- Relationship modelling
- Dynamic DAX measures
- Granularity-aware filtering logic

This improved dashboard consistency and ensured slicers interacted correctly across all report pages.

---

# Future Improvements

Potential future enhancements include:
- Customer Lifetime Value (CLV) modelling
- Cohort retention analysis
- Revenue forecasting
- Automated cloud refresh pipelines
- Customer churn prediction models
- Real-time reporting integration

---

# Skills Demonstrated

## Technical Skills
- SQL
- BigQuery
- Power BI
- DAX
- Power Query
- Data Modelling
- ETL Processes

## Analytical Skills
- RFM Segmentation
- Revenue Analysis
- Customer Retention Analysis
- KPI Development
- Product Performance Analysis

## Business Skills
- Data Storytelling
- Stakeholder Reporting
- Business Intelligence
- Operational Decision Support

---

# Project Screenshots

## Executive Business Summary
<img width="1292" height="720" alt="rfm1" src="https://github.com/user-attachments/assets/9dc32de4-ae61-49d9-880c-905fd59719a0" />


## Customer Segments & Retention Risk
<img width="1295" height="736" alt="rfm2" src="https://github.com/user-attachments/assets/4616d7e3-76e4-4a4b-b016-0de4a3fca186" />


## Product & Growth Opportunities
<img width="1287" height="727" alt="rfm3" src="https://github.com/user-attachments/assets/4e2f3241-7cca-413b-8bad-d60a09455ee1" />


---

# Author

## Nwafor Franklin
Information Systems Analyst | Data Analytics Consultant

- LinkedIn: https://linkedin.com/in/nwaforfranklin100
- GitHub: https://github.com/fhranklyndre
