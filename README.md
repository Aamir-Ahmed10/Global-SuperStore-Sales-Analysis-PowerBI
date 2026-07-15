# Global Superstore Sales Analysis — Power BI Dashboard

## 📌 Project Overview

This project analyzes four years (2012–2015) of order-level sales data for a global retail superstore operating across **5 markets, 23 regions, and 165 countries**. Using a raw transactional dataset (Orders, Returns, and People tables), the goal was to build a single-page Power BI dashboard that gives leadership a fast, visual read on **sales performance, profitability, customer value, and fulfillment/returns health** — and to surface the specific product, geography, and pricing issues that are quietly eating into margin.

## 🧰 Tools & Tech

- **Power BI Desktop** — data modeling, DAX measures, dashboard/report
- **Excel** — source dataset 
- **Python / pandas** — used here to validate the underlying numbers


## 🗂️ The Dataset

| Table | Rows | Description |
|---|---|---|
| **Orders** | 51,290 | Order line items: dates, ship mode, customer, geography, product, sales, quantity, discount, profit, shipping cost, priority |
| **Returns** | 1,079 | Which order IDs were returned, and from which region |
| **People** | 24 | Regional manager assigned to each of the 24 sales regions |

Time span: **Jan 2012 – Dec 2015**. Grain: one row per product line per order (51,290 lines roll up to 25,728 unique orders).

## ❓ Business Questions This Dashboard Is Built to Answer

A stakeholder looking at this dashboard would naturally ask:

1. What are our total sales, profit, and units sold — and what's our overall margin?
2. Is the business growing year over year, or flat/declining?
3. Which markets and regions generate the most (and least) revenue and profit?
4. Are there regions where we're *selling* well but actually *losing* money?
5. Which products are our best profit drivers, and which ones are actively losing us money?
6. Which customer segment (Consumer / Corporate / Home Office) matters most to the business?
7. Who are our most valuable customers, and are they worth a retention/loyalty push?
8. How fast are we fulfilling orders on average, and does shipping mode affect that?
9. What percentage of orders are being returned, and is it concentrated anywhere?
10. Is our discounting strategy helping drive sales, or quietly destroying profit?

## 🔍 Key Findings

**Overall performance (2012–2015)**
- Total Sales: **$12.64M** | Total Profit: **$1.47M** | Overall margin: **11.6%**
- Units sold: **178,312** across 25,728 unique orders
- Average delivery time: **~4.0 days**
- Return rate: **~4.2%** of orders were returned

**Growth trend**
- Sales nearly **doubled** from 2012 ($2.26M) to 2015 ($4.30M), with profit growing in step (~$249K → ~$504K) — the business is on a healthy, consistent upward trajectory, not a one-year spike.

**Profitability by category**
- **Technology** is the strongest category ($4.74M sales, $664K profit, ~14% margin).
- **Office Supplies** is next most efficient ($3.79M sales, $519K profit, ~13.7% margin).
- **Furniture** is the weak link: $4.11M in sales but only $285K profit (~7% margin) — dragged down almost entirely by the **Tables** sub-category, which lost **-$64K** despite $757K in sales.

**Geography**
- **Asia Pacific** ($4.04M) and **Europe** ($3.29M) are the top two markets by sales; **Africa** is the smallest ($0.78M).
- Most regions are profitable, but a few are quietly bleeding money: **Western Asia (-$54K)**, **Western Africa (-$50K)**, and **Central Asia (-$7K)** all post *negative* overall profit despite generating real sales — these are the regions the map/slicer combination is designed to expose.

**Products**
- Top profit drivers: Canon imageCLASS 2200 Copier (+$25.2K), Cisco and Motorola smartphones (+$17K each), and a couple of premium furniture/appliance items.
- Biggest losses: Cubify CubeX 3D Printers (-$8.9K and -$3.8K for two variants), a Lexmark laser printer (-$4.6K), a cordless Motorola phone (-$4.4K), and two Bevis tables — a recurring pattern of **high-ticket electronics and tables losing money**, not small accessories.

**Customers**
- The top 10 customers each contribute **$6.3K–$8.7K** in individual profit (led by Tamara Chand and Raymond Buch) — a small, identifiable group worth a dedicated retention/loyalty strategy.
- **Consumer** is the largest and most profitable segment (51% of sales, $749K profit), ahead of Corporate ($441K) and Home Office ($277K).

**Discounting**
- Discount and profit are **negatively correlated (-0.32)** — the more heavily an order is discounted, the less profitable it tends to be. Combined with the loss-making products above, this points to a discount policy that isn't being applied selectively enough.

**Fulfillment**
- **Standard Class** is the dominant shipping mode (60% of all orders), which is consistent with the ~4-day average delivery time. Faster modes (Same Day, First Class) exist but are used far less often, suggesting delivery speed isn't currently a differentiator being pushed to customers.

## ✅ What This Suggests for the Business

- **Investigate Furniture Tables and the loss-making electronics** (3D printers, specific phone/printer models) — either renegotiate cost/supplier pricing, reduce discount depth on these specific SKUs, or reconsider carrying them.
- **Audit discount policy** in Western Asia, Western Africa, and Central Asia specifically — these regions have sales volume but negative profit, which is a pricing/discounting problem more than a demand problem.
- **Build a retention program around the top 10–20 customers** identified in the dashboard; they're a disproportionate share of profit.
- **Lean into Technology and Office Supplies growth** given they're both the highest-margin and (for Technology) highest-revenue categories.


## 📈 Possible Next Steps

- Add a discount-threshold analysis (profit vs. discount band) as its own visual.
- Build a customer RFM (Recency/Frequency/Monetary) segmentation page.
- Add a returns-by-category breakdown to see if returns are concentrated in specific product types.

## 👤 Author

Aamir Ahmed, https://www.linkedin.com/in/aamir-ahmed10/
