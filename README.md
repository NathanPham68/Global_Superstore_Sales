# [POWER BI] How to Monitor Net Sales Effectively – Sales Performance Analysis

<img width="960" height="383" alt="image" src="https://github.com/user-attachments/assets/92f55a0a-fa65-4fff-b706-5657cf91d9dc" />

## Table of Contents
I. [📌 Introduction](#i.-introduction)

II. [📂 Design Thinking Method](#ii.-design-thinking-method)

III. [🧠 Visualization](#iii.-visualization)

IV. [📊 Insights & Recommendations](#iv.-insights-&-recommendations)

## I. Introduction
### 📖 **What is the purpose of this project?**

This project centers on building a Power BI dashboard using the Global Superstore Sales dataset, which includes information on orders, sales representatives and product returns. Its primary goal is to provide senior managers with actionable insights to assess performance, identify growth opportunities, focus on strategic products, and make informed decisions that enhance revenue and Return on Investment (ROI).

### ❓ **Business Questions:**

✔️ How is Superstore currently performing?

✔️ Which markets offer the best opportunities for expansion to drive revenue and ROI?

✔️ What products should be prioritized for strategic growth?

### 👤 **Who is this project for?**

✔️ Data and business analysts looking for actionable insights.

✔️ Marketing and sales teams focusing on product performance and market development.

✔️ Route-to-market teams aiming to enhance distribution efficiency and market penetration.

### 🎯 **Project Outcome:**

- Revenue saw strong growth, but profit margins stayed flat, suggesting increased costs and minimal efficiency improvements.  
- Canada stood out as a high-margin market (28%) despite generating lower revenue, while Africa and EMEA had the highest YoY growth, signaling strong expansion potential.  
- Oceania and Africa led in acquiring new customers, though most revenue continued to come from loyal repeat buyers.  
- The Technology category drove both revenue and profit growth, though high return rates for specific SKUs (e.g., Cisco, Motorola) affected margins.  
- Products like Copiers delivered the highest profit per unit, whereas low-performing items (e.g., Supplies, Furnishings) diluted overall profitability.

By aligning regional and product strategies, senior managers can **scale in high-margin markets**, **invest in scalable profitable categories**, and **optimize acquisition and return management**, driving **sustainable long-term growth**.

### 📂 **Introduction to Dataset**

The Dataset consists of 3 data tables:

<details>
<summary> <strong>Table 1: Orders (Fact order)</strong></summary>

🛒 **Orders** – Contains detailed transaction and customer information (**51,290 records**).

| Column Name       | Data Type   | Description                              |
|------------------|------------|------------------------------------------|
| `Order ID`      | `VARCHAR`   | Unique identifier for each order.       |
| `Order Date`    | `DATE`      | Date when the order was placed.         |
| `Ship Date`     | `DATE`      | Date when the order was shipped.        |
| `Ship Mode`     | `VARCHAR`   | Shipping method used for delivery.      |
| `Customer ID`   | `VARCHAR`   | Unique identifier for each customer.    |
| `Customer Name` | `VARCHAR`   | Full name of the customer.              |
| `Segment`       | `VARCHAR`   | Customer segment (e.g., Consumer, Corporate). |
| `City`         | `VARCHAR`   | City where the order was placed.        |
| `State`        | `VARCHAR`   | State where the order was placed.       |
| `Country`      | `VARCHAR`   | Country where the order was placed.     |
| `Postal Code`  | `VARCHAR`   | Postal code of the shipping address.    |
| `Market`       | `VARCHAR`   | Market region (e.g., APAC, EMEA).       |
| `Region`       | `VARCHAR`   | Geographical region of the order.       |
| `Product ID`   | `VARCHAR`   | Unique identifier for each product.     |
| `Category`     | `VARCHAR`   | Product category (e.g., Furniture, Office Supplies). |
| `Sub-Category` | `VARCHAR`   | Sub-category of the product.            |
| `Product Name` | `VARCHAR`   | Name of the product ordered.            |
| `Sales`        | `DECIMAL`   | Revenue generated from the order.       |
| `Quantity`     | `INT`       | Number of items ordered.                |
| `Profit`       | `DECIMAL`   | Profit earned from the order.           |

</details>

<details>
<summary> <strong>Table 2: Returns (Information of Returned orders)</strong></summary>

🔄 **Returns** – Stores data on returned orders.

| Column Name  | Data Type | Description |
|--------------|-----------|-------------|
| `Returned`   | `VARCHAR` | Indicates whether the order was returned (e.g., 'Yes' or 'No'). |
| `Order ID`   | `VARCHAR` | Unique identifier for each order. |

</details>

<details>
<summary> <strong>Table 3: People (Information of Sales person)</strong></summary>

👥 **People** – Holds information about sales representatives.

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| `Person`    | `VARCHAR` | Name of the salesperson. |
| `Region`    | `VARCHAR` | Geographic region where the salesperson operates. |

</details>

## II. Design Thinking Method
This project applies the Design Thinking framework to ensure the solution deeply aligns with stakeholder needs.

![image](https://github.com/user-attachments/assets/2dbcf783-46f6-4f09-8bb4-318f936548d9)

✅ Step 1 – Empathize

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/a24ab2eb-4a69-4fd3-b917-4a680c59ec2e" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1dfb5926-f3a7-4b3d-9a34-422e190bc27d" />

✅ Step 2 – Define

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/d82b5c9e-0eaa-4de7-9398-46ae462bc3c3" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e57d9f74-504d-4c24-8e49-3041c125cca3" />

✅ Step 3 – Ideate

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/75b96b8f-48f9-4540-9666-99a686c63986" />

✅ Step 4 & 5 – Prototype & Review

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/1aa64e38-c084-4a10-aa33-22b0cd72be89" />

## III. Visualization
### 1. Entity Relationship Diagram Model

<img width="1032" height="659" alt="image" src="https://github.com/user-attachments/assets/c1bd3315-ad68-4f8b-b403-4d8e649c1671" />

### 2. Summary

<img width="1333" height="753" alt="image" src="https://github.com/user-attachments/assets/db2502be-08b3-48e8-bc64-579ba33db270" />

* Total profit margin is moderate and stable across years, but has not improved significantly—indicating increased costs or operational inefficiencies.

* Q4 consistently shows the highest revenue and order quantity, suggesting strong seasonal demand.

* Returning customers dominate total revenue, while new customer acquisition is limited to certain regions like Oceania and Africa.

### 3. Market

<img width="1333" height="753" alt="image" src="https://github.com/user-attachments/assets/96d8c311-0932-4645-aa03-b8b6417b3b36" />

* Canada leads with the highest profit margin (26.62%) and 0% return rate, making it the most profitable and efficient market.

* EMEA shows lowest profit margin (5.45%), mainly due to extreme negative margins in specific countries.

* If underperforming countries are removed, EMEA’s adjusted margin reaches 23.89%, second only to Canada.

### 4. Product

<img width="1333" height="756" alt="image" src="https://github.com/user-attachments/assets/36a2a0ca-8488-4c86-a1b6-9a07a3c76ff8" />

* Copiers is the most profitable sub-category (35.68% profit margin).

* Other high-margin products include: Tables, Labels, Envelopes, Fasteners, Accessories, Storage.

* Categories like Supplies, Art, Machines have significantly lower margins.

### 5. Net sales

<img width="1333" height="757" alt="image" src="https://github.com/user-attachments/assets/46437a22-5de8-471b-914f-63559b3a9854" />

* Technology leads in revenue, but faces higher return rates, especially with brands like Cisco and Motorola.

* Top-selling products (e.g., Canon imageCLASS) contribute significantly to profit.

* Some SKUs such as Cubify CubeX 3D Printers are consistently unprofitable.

## IV. Insights & Recommendations

### Insights

The analysis revealed several key patterns in sales and operations:

* Top-performing regions and customer segments significantly contribute to overall revenue, while certain markets underperform consistently.

* Profitability is not directly tied to sales volume — some high-sales categories have low or even negative profit margins.

* Returns are concentrated in specific product categories and regions, indicating potential quality or service issues.

* Sales trends fluctuate seasonally, and specific months consistently outperform others, suggesting opportunities for targeted promotions.

* Sales representatives' performance varies widely by region, with some outperforming peers in similar conditions.

### Recommendations

* Refocus marketing and sales efforts on high-margin products and profitable customer segments to maximize ROI.

* Investigate root causes of high return rates in key categories and implement corrective actions such as product quality reviews or better customer education.

* Optimize inventory and staffing based on seasonal trends to improve efficiency and responsiveness.

* Launch training or support programs for underperforming sales reps to enhance overall team performance.

* Explore market expansion in regions with steady growth potential and proven customer demand.


