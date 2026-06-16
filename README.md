# 🎯 Customer Personality Analysis: Marketing Campaign Insights

## 🚀 Project Overview
This project performs a deep-dive **Customer Personality Analysis** to understand customer behaviors and optimize marketing efficiency. By analyzing a dataset of **2,240 customers**, we aim to transition from "mass marketing" to **"targeted marketing"**—delivering the right message to the right segment to maximize ROI.

The project features a full end-to-end pipeline: **Data Extraction** ➡️ **Cleaning & Standardizing** ➡️ **Strategic Visualization**.

---

## 🗂 Dataset Architecture (Standardized Schema)
The analysis is based on the dataset `1.marketing_campaign.csv`. All features have been standardized to **snake_case** for better programmatic access and consistency.

### 1. Customer Profile (Demographics)
* **Identity:** `customer_id`, `year_birth`, `education`, `marital_status`, `income`.
* **Family:** `kidhome` (Small children), `teenhome` (Teenagers).
* **Loyalty:** `dt_customer` (Enrollment date), `recency` (Days since last purchase), `complain`.

### 2. Product Preferences (Spending - "Amount" Series)
* **Monetary Value:** Total spent in the last 2 years on:
    * `amount_wines`, `amount_fruits`, `amount_meat_products`
    * `amount_fish_products`, `amount_sweet_products`, `amount_gold_prods`.

### 3. Promotion & Campaign Response
* **Campaign History:** `accepted_campaign_1` through `accepted_campaign_5`.
* **Target Variable:** `response` (1 if customer accepted the offer in the last campaign, 0 otherwise).
* **Deals:** `num_deals_purchases` (Purchases made with a discount).

### 4. Purchasing Channels (Place)
* **Touchpoints:** `num_web_purchases`, `num_catalog_purchases`, `num_store_purchases`, and `num_web_visits_month`.

---

## 🧹 Data Engineering & Transformation
Using **Python (Pandas)**, the raw data underwent a rigorous transformation process to ensure model-ready quality:

* **Naming Standardization:** Converted all 29 original columns (PascalCase) to `snake_case` (e.g., `MntWines` ➡️ `amount_wines`) for professional coding standards.
* **Handling Missing Values:** * Identified missing entries in the `income` column.
    * Applied **Mean Imputation** to fill gaps, preserving the full **2,240** record count.
* **Feature Engineering:**
    * `age`: Derived from `year_birth`.
    * `total_spend`: Aggregated spending across all product categories.
    * `total_children`: Combined `kidhome` and `teenhome`.
* **Data Cleaning:** Detected and addressed outliers in `income` and `year_birth` to prevent statistical bias.

---

## 📈 Key Analytical Focus
The analysis seeks to answer critical business questions:
1. **Segment Response:** Which customer profiles (Age/Income/Education) have the highest `response` rate?
2. **Product Correlation:** How does household size (`kidhome`/`teenhome`) affect spending on `amount_wines`?
3. **Channel Efficiency:** Where do high-income customers shop most? (`num_web_purchases` vs. `num_store_purchases`).
4. **Campaign ROI:** Comparative analysis of `accepted_campaign_1-5` to identify the most successful historical strategy.

---

## 📊 Strategic Power BI Dashboard
The strategic findings are presented in a dynamic dashboard (`Marketing_Campaign_Dashboard.pbix`):

* **Executive Summary:** Real-time tracking of Total Revenue, Conversion Rates, and Customer Count.
* **Customer Clusters:** Visualizing segments based on Income vs. Spending patterns.
* **Campaign Drill-down:** Interactive analysis of acceptance rates for each marketing initiative.
* **Behavioral Insights:** Mapping channel preferences against demographic segments.

---
## Dashboard
<img width="1468" height="811" alt="Screenshot 2026-06-09 210950" src="https://github.com/user-attachments/assets/d3c215f0-6265-4cb6-a901-971ad2b39558" /


## 🧪 Tech Stack
* **Language:** Python 3.x
* **Libraries:** Pandas
* **Visualization:** Power BI Desktop
* **IDE:** Visual Studio Code
* **Version Control:** Git & GitHub


