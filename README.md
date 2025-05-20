# E-Commerce Product Performance Dashboard & Analysis 📊

[Dashboard Overview](Dashboard.pdf)

## Overview
As a non-technical professional transitioning to a data analyst role, I built this project to demonstrate my skills in data cleaning, exploratory data analysis (EDA), and visualisation. This project analyses a synthetic e-commerce dataset to understand sales patterns, customer preferences, and factors influencing return rates. I created interactive dashboards in Power BI to visualise product performance and category-wise trends, delivering actionable insights to optimise pricing, reduce returns, and improve stock and delivery planning.

---

## Objective 🔖
- Analyse an e-commerce dataset focusing on price, ratings, returns, and delivery trends.
- Identify top-performing products and categories in terms of revenue and profit.
- Understand customer behaviour through EDA and visualisations.
- Create interactive dashboards in Power BI to present findings.
- Deliver business insights to optimise pricing, reduce return rates, and improve stock and delivery strategies.

---

## Dataset 💡
- **Source**: [E-Commerce Product Performance Dataset (Kaggle)](https://www.kaggle.com/datasets) (synthetic dataset)
- **Rows**: 2,000 products
- **Columns**:
  - `Product_Price`: Price in USD (5 to 1000)
  - `Discount_Rate`: Discount applied (0.0 to 0.8)
  - `Product_Rating`: Customer rating (1 to 5)
  - `Number_of_Reviews`: Total reviews (0 to 5000, highly skewed)
  - `Stock_Availability`: In stock (1) or out of stock (0)
  - `Days_to_Deliver`: Delivery time (1 to 30 days)
  - `Return_Rate`: Proportion of returns (0.0 to 0.9)
  - `Category_ID`: Product category (1 to 10)

The dataset was cleaned by handling missing values (~5% initially), verifying outliers, and ensuring no duplicates.

---

## Key Questions 📈
- Which products generate the most profit?
- Is there a correlation between views, cart adds, and purchases?
- Which products have the highest conversion rates?
- What categories perform best in terms of revenue and profit?

---

## Tools & Technologies 🛠️
- **Python**: Data cleaning and EDA
  - **Pandas & NumPy**: Data manipulation
  - **Matplotlib & Seaborn**: Static visualizations
  - **Plotly**: Interactive plots
- **Power BI**: Interactive dashboards for final visualizations
- **Jupyter Notebook**: For coding and documentation

![Python](https://img.shields.io/badge/Python-3.8-blue) ![Power BI](https://img.shields.io/badge/Power%20BI-Desktop-yellow)

---

## Project Workflow
1. **Data Cleaning**:
   - Handled missing values (~5% initially, none in final dataset).
   - Verified outliers using boxplots (all within expected ranges).
   - Removed duplicates (none found).
   - Formatted `Stock_Availability` (binary: 0 or 1, with 1816 in stock, 184 out of stock).

2. **Exploratory Data Analysis (EDA)**:
   - Visualised distributions (e.g., `Product_Price` is right-skewed, `Product_Rating` is left-skewed).
   - Analysed relationships (e.g., no strong correlations; highest: 0.0426 between `Discount_Rate` and `Number_of_Reviews`).
   - Explored `Category_ID` vs `Return_Rate`, `Discount_Rate` vs `Return_Rate`, and `Days_to_Deliver` vs `Return_Rate`.

3. **Dashboards**:
   - Created two interactive dashboards in Power BI to visualise findings.

---

## Key Findings
- **Distributions**:
  - `Product_Price`: Most products priced below 200 USD (mean: 156.62 USD).
  - `Product_Rating`: Most ratings around 4.0–4.5 (mean: 3.73), indicating good customer satisfaction.
  - `Number_of_Reviews`: Most products have fewer than 500 reviews (mean: 299.60).
  - `Return_Rate`: Most values below 0.5 (mean: 0.3278).
- **Relationships**:
  - Products with 40–60% discounts have the highest return rate (0.3408), while 60–80% discounts have a lower return rate (0.3113).
  - Shorter delivery times (0–10 days) have a slightly higher return rate (0.3346) than longer times (20–30 days, 0.3203).
- **Category Insights**:
  - Categories 3, 5, and 10 have the highest return rates (0.3411, 0.3353, 0.3357).
  - Category 10 has the highest average price (170.08 USD), possibly leading to higher expectations and returns.
  - Category 3 has the highest average reviews (351.87), suggesting that higher purchase volume contributes to more returns.
- **Stock Impact**:
  - In-stock and out-of-stock products have similar ratings (3.7319 vs 3.7331), showing that stock status doesn’t impact satisfaction.

---

## Answers to Key Questions
- **Which products generate the most profit?**
  - Without profit data, `Product_Price` and `Return_Rate` were used as proxies. Category 10 (average price: 170.08 USD) might generate high revenue, but has a high return rate (0.3357). Category 2 (lowest return rate: 0.3091) could be more profitable.
- **Is there a correlation between views, cart adds, and purchases?**
  - Using `Number_of_Reviews` as a proxy for engagement, correlations are weak (e.g., 0.0426 with `Discount_Rate`).
- **Which products have the highest conversion rates?**
  - Using `Number_of_Reviews` as a proxy for purchases, Category 3 has the highest reviews (351.87), but its high return rate (0.3411) suggests post-purchase dissatisfaction.
- **What categories perform best in terms of revenue and profit?**
  - Categories 3 and 10 likely have higher revenue (higher prices and reviews: 162.27 USD/351.87 reviews for Category 3, 170.08 USD/327.58 reviews for Category 10). Category 2 (lowest return rate) could be more profitable.

---

## Business Insights 💼
- **Reduce Returns**: Investigate Categories 3, 5, and 10 for quality or expectation mismatches. Category 10’s higher prices might lead to stricter expectations.
- **Discount Strategy**: Avoid 40–60% discounts unless clearing inventory, as they lead to higher returns (0.3408). Very high discounts (60–80%) have lower returns (0.3113).
- **Delivery Planning**: Shorter delivery times (0–10 days) have higher return rates (0.3346). Manage expectations for fast deliveries to reduce impulse returns.
- **Stock Management**: Stock status doesn’t affect ratings, so prioritise stocking high-demand categories like Category 3.

---

## Dashboards in Power BI 📈
- **Product Performance Dashboard**: Includes a bar chart of `Product_Price` and `Return_Rate` by `Category_ID`, and a scatter plot of `Number_of_Reviews` vs `Return_Rate`.
  - Screenshot: [Product Performance Dashboard](Dashboard.pdf)
  - Power BI File: [Download Power BI File](Dashboard.pbix)
  <!-- View Online: [Power BI Dashboard](your_power_bi_link)  Replace with actual link -->
- **Category Insights Dashboard**: Features a pie chart of product distribution by `Category_ID`, a line chart of `Return_Rate` by `Days_to_Deliver` bins, and a table of top categories by estimated revenue (price * reviews).
  - Screenshot: [Category Insights Dashboard](Dashboard.pdf)
  - Power BI File: [Download Power BI File](Dashboard.pbix)
  <!--  View Online: [Power BI Dashboard](your_power_bi_link)  Replace with actual link -->

---

## How to Run This Project 🚀
1. Clone this repository:
   ```bash
   git clone [https://github.com/AmitKumar-001/E-Commerce-Product-Performance-Dashboard-Analysis/blob/main/eCommerce_Product_Performance.ipynb](https://github.com/AmitKumar-001/E-Commerce-Product-Performance-Dashboard-Analysis/blob/main/eCommerce_EDA.ipynb)
   
