# [POWER BI] Global_Superstore_Sales

<img width="960" height="383" alt="image" src="https://github.com/user-attachments/assets/92f55a0a-fa65-4fff-b706-5657cf91d9dc" />

## I. Introduction
### 1. Introduction to Dataset
This project aims to develop a comprehensive business intelligence dashboard for a global retail company using three core datasets.
The dashboard empowers senior managers to gain a clear view of overall sales performance, profit trends, customer behavior, product performance, and return rates — enabling data-driven decisions for market expansion and strategic product focus.
* Consists of 3 data tables:
  - Table 1: Orders: Fact order
  - Table 2: People: Information of Sales person
  - Table 3: Returns: Information of Returned orders

### 2. Data Dictionary

![image](https://github.com/user-attachments/assets/3ec09aea-f6f6-4b89-bb32-bf197a39fe02)

## II. Design Thinking Method
This project applies the Design Thinking framework to ensure the solution deeply aligns with stakeholder needs.

![image](https://github.com/user-attachments/assets/2dbcf783-46f6-4f09-8bb4-318f936548d9)

✅ Step 1 – Empathize
* Understand the needs, behaviors, and challenges of senior managers.

* They require an overview of global sales, profit, and returns, with the ability to drill down by region, product, and customer segment.

* Pain points include scattered data, time-consuming reports, and lack of actionable insights.

✅ Step 2 – Define

Define the key business questions:

* Which products and regions are driving the most revenue?

* Where are profit margins strong or weak?

* Which customers or markets have high return rates?

* How is the business performing over time?

✅ Step 3 – Ideate

* Identify the best metrics and dimensions:

Metrics: Total Sales, Total Profit, Total Orders, Profit Margin, Return Rate.

Dimensions: Region, Country, City, Product Category, Sub-Category, Customer Segment, Order Date.

* Brainstorm visual layouts: KPI cards, trend lines, pie charts by category/market, maps by country/city, top/bottom product lists.

✅ Step 4 – Prototype

Build a Power BI dashboard with:

* Summary page (KPIs & geographic map)

* Details page (breakdowns by category, segment, ship mode, top products/customers)

* Database page (raw transaction table for deep-dive analysis)

✅ Step 5 – Review

* Test the dashboard with stakeholders.

* Gather feedback on usability, clarity, and actionable insights.

* Refine filters, visuals, and drill-down paths based on real user feedback.

## III. Visualization

### 1. Summary

![image](https://github.com/user-attachments/assets/c13deb26-ad8d-4c1d-9f56-0ad102adc163)

### 2. Details

![image](https://github.com/user-attachments/assets/b785b132-c213-4302-ab3d-879ef676732b)

### 3. Database

![image](https://github.com/user-attachments/assets/04b7bc4c-9b8d-4c22-af21-f66813406f91)

## IV. Insights
1) Business Overview

・Total sales: $12.64M, Total profit: $1.47M

→ Profit margin is around 11.6%, which is not very high

=> Profitability should be closely monitored.

・Return rate: 2.29%, which is an acceptable level for global sales.

2) Market Region Analysis

・APAC, EU, LATAM, and EMEA are the four main regions, accounting for the majority of sales.

・United state is the country with the largest number of orders. 

3) Product Category Analysis

・Technology accounts for the highest sales (37.53%) → It is the core product category.

・Office Supplies and Furniture also contribute significantly, though to a lesser extent.
However, some technology products are heavily unprofitable (e.g., Cubby Cubex 3D) → these should be reviewed for potential removal or strategic adjustment.

4) Top Products and Customers

・Canon ImageCLASS and Cisco Smart Phone are the most profitable products.

・Top 5 customers generate consistent profits (from $7.4k to $8.6k) → These are VIP customers who require special attention.

5) Growth Trends

・Sales and profits showed positive growth year-over-year from 2011 to 2014, especially strong starting in 2013 → A positive trend.

6) Logistics

・Average delivery time: 3.97 days

・Returned orders are not negligible (1,172 orders) → Needs further investigation (product quality? delayed delivery?)

## V. Recommendations
1) Focus on High-Potential Markets

・Strengthen presence in APAC and EU, which already show strong sales and have further potential.

・Prioritize expansion in EMEA, as it holds a significant market share but hasn't seen explosive growth yet.

2) Optimize Product Portfolio

・Continue investing in high-margin technology products.

・Review and remove or improve loss-making products (e.g., Cubby Cubex 3D).

・Consider upselling / cross-selling Office Supplies and Furniture to technology customers.

3) Nurture VIP Customers

・Design special loyalty programs for high-profit customers (e.g., Bill Eplett, Hunter Lopez, etc.).

・Provide faster delivery and better after-sales support for this customer segment.

4) Improve Logistics and Return Control

・Conduct deeper analysis into the reasons for product returns to improve product quality or service.

・Enhance order tracking and ensure more accurate delivery commitments.

