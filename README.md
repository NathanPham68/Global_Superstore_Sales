# [POWER BI] Global_Superstore_Sales

<img width="960" height="383" alt="image" src="https://github.com/user-attachments/assets/92f55a0a-fa65-4fff-b706-5657cf91d9dc" />

## Table of Contents
I. [📌 Introduction](#i.-introduction)
II. [📂 Design Thinking Method](#ii.-design-thinking-method)
III. [🧠 Visualization](#iii.-visualization)
IV. [📊 Insights & Recommendations](#iv.-insights-&-recommendations)

## I. Introduction
📌 **Objective:**

**📖 What is the purpose of this project?**

This project focuses on developing a Power BI dashboard utilizing the Global Superstore Sales dataset, which contains data on Orders (transactions), People (sales representatives), and Returns (product returns).
The main objective is to equip senior managers with data-driven insights to:

- Evaluate current business performance
 
- Refine strategies for market expansion

- Highlight key products for strategic growth

- Enable more informed decision-making to boost revenue and Return on Investment (ROI)


👤 **Who is this project for?**

✔️ Data and business analysts looking for actionable insights.

✔️ Marketing and sales teams focusing on product performance and market development.

✔️ Route-to-market teams aiming to enhance distribution efficiency and market penetration.


❓ **Business Questions:**

✔️ How is Superstore currently performing?

✔️ Which markets offer the best opportunities for expansion to drive revenue and ROI?

✔️ What products should be prioritized for strategic growth?


🎯 **Project Outcome:**

- Revenue saw strong growth, but profit margins stayed flat, suggesting increased costs and minimal efficiency improvements.  
- Canada stood out as a high-margin market (28%) despite generating lower revenue, while Africa and EMEA had the highest YoY growth, signaling strong expansion potential.  
- Oceania and Africa led in acquiring new customers, though most revenue continued to come from loyal repeat buyers.  
- The Technology category drove both revenue and profit growth, though high return rates for specific SKUs (e.g., Cisco, Motorola) affected margins.  
- Products like Copiers delivered the highest profit per unit, whereas low-performing items (e.g., Supplies, Furnishings) diluted overall profitability.

By aligning regional and product strategies, senior managers can **scale in high-margin markets**, **invest in scalable profitable categories**, and **optimize acquisition and return management**, driving **sustainable long-term growth**.


📂 **Introduction to Dataset**
This project aims to develop a comprehensive business intelligence dashboard for a global retail company using three core datasets.
The dashboard empowers senior managers to gain a clear view of overall sales performance, profit trends, customer behavior, product performance, and return rates — enabling data-driven decisions for market expansion and strategic product focus.
* Consists of 3 data tables:
  - Table 1: Orders: Fact order
  - Table 2: People: Information of Sales person
  - Table 3: Returns: Information of Returned orders

📝 **Data Dictionary**

![image](https://github.com/user-attachments/assets/3ec09aea-f6f6-4b89-bb32-bf197a39fe02)

<details>
<summary> <strong>Table 1: Orders</strong></summary>

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
<summary> <strong>Table 2: Returns</strong></summary>

🔄 **Returns** – Stores data on returned orders.

| Column Name  | Data Type | Description |
|--------------|-----------|-------------|
| `Returned`   | `VARCHAR` | Indicates whether the order was returned (e.g., 'Yes' or 'No'). |
| `Order ID`   | `VARCHAR` | Unique identifier for each order. |

</details>

<details>
<summary> <strong>Table 3: People</strong></summary>

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

<img width="1333" height="754" alt="image" src="https://github.com/user-attachments/assets/7649d291-6f3d-485d-9984-982b0174c09f" />

### 3. Market

<img width="1333" height="755" alt="image" src="https://github.com/user-attachments/assets/caf1bb58-dc66-42ea-befa-dd7dfaf5c00a" />

### 4. Product

<img width="1337" height="754" alt="image" src="https://github.com/user-attachments/assets/0afae075-e485-4084-b6b9-d15abbbf1505" />

### 5. Net sales

<img width="1336" height="754" alt="image" src="https://github.com/user-attachments/assets/b55e3f2d-0c1d-45ce-a4fe-c6a68749bc0b" />

## IV. Insights & Recommendations
1) Canada is the most profitable market with the highest profit margin (around 28%). It also shows zero return rate, making it a highly efficient and low-risk market. Additionally, it maintains consistently high margins across all categories and sub-categories, which makes Canada the top priority for business expansion. A deep dive into the strategies and operations of the Canada market (including resource planning and PIC) is recommended for replication in other regions.

2) EMEA shows an exceptionally low overall profit margin (~5.45%), much lower than other regions. Upon closer inspection, some countries within EMEA report severely negative profit margins, dragging down the entire region’s performance. Notable underperformers include:

・Turkey (-90.72%), Tajikistan (-108.03%), Lithuania (-128.94%), Kazakhstan (-144.28%), UAE (-156.09%), Yemen (-162.17%), and Turkmenistan (-171.54%).

・These countries consistently show poor performance across categories and years. If these outliers are excluded, EMEA's adjusted profit margin would rise to ~23.89%, making it the second most profitable region after Canada. Caution and strategic review are necessary before investing further in these markets.

3) Copiers is the most profitable sub-category, with a profit margin of 35.68%, making it an ideal candidate for further business expansion. Other sub-categories with above-average margins include:

・Tables (35.34%), Labels (30.67%), Envelopes (30.18%), Fasteners (29.23%), Accessories (28.96%), Appliances (28.13%), Storage (27.51%), Chairs (26.74%), Phones (26.57%), and Binders (25.45%).
Focused investment in these profitable categories can help increase overall profitability.

4) Sales and order quantities show strong seasonal and cyclical trends: Q4 consistently outperforms other quarters each year. Year-over-year sales and profits also steadily increase. This trend provides an opportunity to build accurate forecasting models for revenue and resource planning. Adequate preparation in terms of inventory, manpower, logistics, and capital will ensure smooth operations during peak seasons.

5) Technology is the leading category in terms of net sales and profitability, but also has higher return rates in certain SKUs (e.g., Cisco, Motorola) that slightly impact overall margins. Quality control and return management strategies should be enhanced in this area.

6) Products like Canon imageCLASS and Cisco Smart Phones contribute the most profit. Conversely, products such as Cubify CubeX 3D Printers and Bevis Round Tables yield the largest losses. The business should consider discontinuing or repositioning low-performing products.

7) In terms of customer segmentation, returning customers account for the majority of revenue, while new customers are mostly from Oceania and Africa. These regions show high acquisition potential, and targeted marketing campaigns could help boost growth there.

8) Standard Class shipping is the most used method (60.06% of sales), but First Class and Second Day offer slightly better profitability. The company should assess logistics costs vs. customer value to optimize shipping strategy.

9) At the market level, while Canada ranks highest in profit margin, Africa and EMEA show the highest YoY growth. These markets may offer strong long-term growth potential if challenges are managed strategically.

10) Lastly, the overall return rate is 2.29%, and total unique products exceed 10,000 SKUs, indicating a diverse product portfolio. However, not all products contribute equally to profit—there is potential for SKU rationalization to boost efficiency and margins.
