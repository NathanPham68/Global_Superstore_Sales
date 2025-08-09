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

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/86f33f38-b781-4cb9-acf2-2cf60a4fae0f" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/ccea557c-6791-4db2-80b1-a578959f6735" />

✅ Step 2 – Define

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/df2c5159-db08-4fac-85e6-98da29d14bc3" />

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/68a8b8f4-8d5b-4357-b50d-96139c469fbd" />

✅ Step 3 – Ideate

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/64590c92-7f2f-4821-adf8-612182b6bf27" />

✅ Step 4 & 5 – Prototype & Review

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/96053501-e0c9-4cd2-ad93-1b8e8a048f88" />

## III. Visualization
### 1. Entity Relationship Diagram Model

<img width="1032" height="659" alt="image" src="https://github.com/user-attachments/assets/c1bd3315-ad68-4f8b-b403-4d8e649c1671" />

### 2. Summary

<img width="1333" height="821" alt="image" src="https://github.com/user-attachments/assets/727889a6-f8f4-4ce5-ad75-12781ead6832" />

* Total profit margin is moderate and stable across years, but has not improved significantly—indicating increased costs or operational inefficiencies.

* Q4 consistently shows the highest revenue and order quantity, suggesting strong seasonal demand.

👉🏻 Leverage Q4 seasonal peaks through targeted marketing campaigns, bundled offers, and stock optimization.

* Returning customers dominate total revenue, while new customer acquisition is limited to certain regions like Oceania and Africa.

👉🏻 Develop regional acquisition strategies with tailored product mixes to penetrate markets where new customer growth is low.

### 3. Market

<img width="1333" height="823" alt="image" src="https://github.com/user-attachments/assets/99625ba4-d2bb-4bb5-bf17-fbbec3dab6de" />

* Canada leads with the highest profit margin (26.62%) and 0% return rate, making it the most profitable and efficient market.

* EMEA shows lowest profit margin (5.45%), mainly due to extreme negative margins in specific countries.

* Other markets show moderate performance, with certain high-growth potential areas still underdeveloped.

* **Markets Recommended for Expansion:** Canada, High-Performing Countries in EMEA, High-Growth Emerging Markets in APAC & LATAM

* Recommended Strategies by Market Type
  * **Mature & Highly Profitable Markets** (e.g., Canada)
    
    - Double down on customer loyalty programs to retain high-value customers.

    - Introduce premium product lines and bundled offers to increase Average Order Value (AOV).

    - Maintain operational excellence to sustain the low return rate.

  * **Selective Expansion Markets** (Profitable countries in EMEA, parts of APAC/LATAM)
    
    - Localized Product Strategy: Adapt product assortments to local preferences.
    
    - Targeted Marketing: Use regional data to run culturally relevant campaigns.
    
    - Strategic Partnerships: Work with local distributors to reduce market entry risks.

  * **Underperforming or Loss-Making Markets**

    - Conduct deep profitability audits to identify structural issues (pricing, logistics, product fit).
    
    - Reduce or exit markets with persistently negative margins unless there is a clear turnaround plan.
    
    - Shift focus to digital sales channels to lower operational costs and test market responsiveness.

### 4. Product

<img width="1333" height="815" alt="image" src="https://github.com/user-attachments/assets/c34ee793-45ab-4446-bbc0-bb1737780e40" />

* Paper is the most profitable sub-category (23.93% profit margin).

* Other high-margin products include: Labels (20.19%), Envelopes (17.05%), Accessories (16.98%), Copiers (16.77%), Binders (16.41%).

👉🏻 Focus sales and promotional efforts on high-margin categories to boost total profitability.

* Categories like Tables, Machines, Supplies, Chairs have significantly lower margins.

👉🏻 Review pricing and sourcing strategies for low-margin products; consider discontinuation or redesign for underperforming SKUs.

### 5. Net sales

<img width="1333" height="821" alt="image" src="https://github.com/user-attachments/assets/f546eb88-6d72-4778-8592-3cf2acc8dcb2" />

* Technology leads in revenue, but faces higher return rates, especially with brands like Cisco and Motorola.

* Top-selling products (e.g., Canon imageCLASS) contribute significantly to profit.

👉🏻 Expand marketing around top-selling, high-profit products to strengthen their market share.

* Some SKUs such as Cubify CubeX 3D Printers are consistently unprofitable.

👉🏻 Discontinue or phase out chronically unprofitable SKUs, reallocating shelf space and marketing spend toward proven performers.

## IV. Insights & Recommendations

## 🔎 Final Conclusion & Recommendation

| **Strategy** | **Insight** | **Recommendation** |
|--------------|-------------|--------------------|
| **🚀 1. Market Expansion Strategy** | - **Canada** remains the most profitable market (**26.62% margin**) with a **0% return rate**, though total revenue is relatively modest.<br> - **EMEA** shows the lowest overall margin (**5.45%**), but after excluding loss-making countries, adjusted margin climbs to **23.89%**.<br> - **North Asia** & **Caribbean** deliver the highest share of **new customers**, though absolute revenue is still small.<br> - **APAC** markets show moderate margins with room for growth. | - **Deepen market penetration in Canada** through upselling and premium offerings.<br> - **Target profitable countries in EMEA** for expansion; restructure or exit persistent loss-makers.<br> - **Increase marketing in North Asia & Caribbean** to convert new customers into loyal buyers.<br> - **Invest in APAC** with localized product strategies. |
| **🛒 2. Product Portfolio Optimization** | - **Paper** lead in profitability (**23.93% margin**), followed by **Labels, Envelopes, Accessories, Copiers, Binders**.<br> - **Tables, Machines, Supplies, Chairs** show consistently low margins.<br> - Certain SKUs (e.g., **Cubify CubeX 3D Printers**) are repeatedly unprofitable.<br> - Technology drives revenue but faces **higher return rates** (Cisco, Motorola). | - **Scale Copier sales** and promote other high-margin subcategories.<br> - **Phase out or reprice** low-margin categories like Supplies and Machines.<br> - **Audit and replace** unprofitable SKUs.<br> - **Reduce return rates** in Technology via better product education and quality checks. |
| **👥 3. Customer Strategy** | - **Returning customers** contribute the majority of total revenue (~99%).<br> - **North Asia** & **Caribbean** show the largest growth in **new customer acquisition**.<br> - Certain regions have strong brand loyalty but low acquisition rates. | - **Implement loyalty and rewards programs** for existing customers.<br> - **Accelerate acquisition in North Asia & Caribbean** via targeted digital campaigns.<br> - **Introduce referral incentives** to blend retention and acquisition efforts. |
| **⚙️ 4. Operational Efficiency** | - **Q4** consistently drives peak revenue and orders, highlighting strong seasonal demand.<br> - **Canada’s operational model** delivers both high profitability and zero returns.<br> - Some markets incur high logistics costs or frequent product returns.<br> - Loss-making regions dilute global average margins. | - **Leverage Q4 seasonality** with pre-holiday promotions and inventory planning.<br> - **Replicate Canada’s operational practices** in other regions.<br> - **Reduce return rates** through improved product descriptions and QA.<br> - **Exit or restructure** chronically unprofitable regions to protect margins. |



