# sales-operations-customer-retention-dashboard
End-to-end sales operations analytics project using SQL, Power Query, and Power BI to analyze revenue, conversion, customer retention, campaign performance, branch productivity, and CRM data quality.
# Sales Operations & Customer Retention Dashboard

## Project Overview

This project is an end-to-end sales operations analytics solution built using SQL, Power Query, and Power BI.

The dashboard was designed to help sales leaders understand:

- Revenue and sales performance
- Lead-to-sale conversion
- Branch and channel performance
- Customer retention and cancellations
- Campaign effectiveness
- Product and customer-segment trends
- CRM data-quality issues
- Sales forecasting and performance risks

The project uses synthetic data created for portfolio and learning purposes. It does not contain confidential company or customer information.

---

## Business Problem

Sales and operations leaders often receive data from multiple systems, including CRM, ERP, marketing, and transactional platforms.

These datasets may contain:

- Missing customer information
- Duplicate records
- Inconsistent sales stages
- Stale opportunities
- Unassigned leads
- Incorrect or missing dates
- Inconsistent product and channel names
- Limited visibility into conversion and retention

The goal of this project was to create a reliable reporting workflow that transforms raw sales data into decision-ready insights.

---

## Project Objectives

1. Clean and standardize sales and customer data.
2. Build repeatable SQL data-quality checks.
3. Track revenue, conversion, retention, and sales productivity.
4. Compare performance across branches, products, channels, and customer segments.
5. Evaluate campaign return on investment.
6. Identify weaknesses in the sales funnel.
7. Detect incomplete or inconsistent CRM records.
8. Provide actionable recommendations to sales leadership.

---

## Tools Used

- **SQL:** Data cleaning, validation, transformation, and KPI analysis
- **Power Query:** Data-type correction, column standardization, and transformation
- **Power BI:** Data modeling, DAX measures, dashboards, and visual reporting
- **Excel:** Source-data review and reconciliation
- **GitHub:** Version control and project documentation

---

## Dataset

The dataset contains synthetic sales and customer activity records.

Example fields include:

- Customer ID
- Lead ID
- Order ID
- Order Date
- Customer Segment
- Product Category
- Sales Channel
- Branch
- Sales Representative
- Revenue
- Cost
- Profit
- Return Status
- Return Reason
- Campaign
- Customer Status
- Renewal Status

No real customer or employer information is included.

---

## Data Cleaning

The following cleaning and validation steps were performed:

- Checked for missing values
- Standardized date fields
- Corrected inconsistent text categories
- Identified duplicate records
- Validated revenue, cost, and profit fields
- Replaced missing return reasons for non-returned orders
- Calculated return dates
- Reviewed invalid or inconsistent sales records
- Created CRM completeness indicators
- Prepared cleaned tables for Power BI

Example SQL:

```sql
SELECT
    COUNT(*) AS total_records,
    COUNT(DISTINCT Customer_ID) AS unique_customers,
    COUNT(DISTINCT Order_ID) AS unique_orders
FROM ecommerce_returns_synthetic_data;
