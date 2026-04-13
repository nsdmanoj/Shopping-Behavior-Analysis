# 🛍️ Shopping Behavior Analysis

A comprehensive end-to-end data analytics project analyzing customer shopping behavior using transactional retail data. The goal is to uncover insights into spending patterns, customer segments, product preferences, and subscription behavior to guide strategic business decisions.

---

## 📌 Problem Statement

A leading retail company wants to better understand its customers' shopping behavior to improve sales, customer satisfaction, and long-term loyalty. Management noticed changes in purchasing patterns across demographics, product categories, and sales channels.

> **Core Question:** *How can the company leverage consumer shopping data to identify trends, improve customer engagement, and optimize marketing and product strategies?*

---

## 📂 Project Structure

```
Shopping-Behavior-Analysis/
│
├── data/
│   └── shopping_behavior.csv              # Raw dataset
│
├── python/
│   └── Shoping_Behaviour_Analysis.ipynb   # Data cleaning & EDA
│
├── sql/
│   └── business_queries.sql               # MySQL business queries
│
├── dashboard/
│   └── Shopping_Behaviour_Analysis.pbix   # Power BI dashboard
│
├── report/
│   └── Shopping_Behavior_Analysis.pdf     # Project report
│
└── README.md
```

---

## 📊 Dataset Summary

| Feature | Detail |
|---|---|
| Total Rows | 3,900 |
| Total Columns | 18 |
| Missing Values | 37 (Review Rating column) |

**Key Features:**
- **Demographics:** Age, Gender, Location, Subscription Status
- **Purchase Details:** Item, Category, Purchase Amount (USD), Season, Size, Color
- **Behavior:** Discount Applied, Previous Purchases, Frequency, Review Rating, Shipping Type

---

## 🔧 Tech Stack

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![MySQL](https://img.shields.io/badge/MySQL-SQL-4479A1?logo=mysql)
![Power BI](https://img.shields.io/badge/PowerBI-Dashboard-F2C811?logo=powerbi)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter)

---

## 🐍 Step 1 — Data Preparation (Python)

Performed in `Shoping_Behaviour_Analysis.ipynb`:

- **Data Loading** — Imported dataset using `pandas`
- **EDA** — Used `df.info()` and `.describe()` for structure and summary stats
- **Missing Data Handling** — Imputed 37 missing `review_rating` values using median per product category
- **Column Standardization** — Renamed all columns to `snake_case`
- **Feature Engineering:**
  - `age_group` — Binned customer ages (Young Adult, Middle-aged, Adult, Senior)
  - `purchase_frequency_days` — Derived from purchase frequency data
- **Consistency Check** — Verified `discount_applied` = `promo_code_used`; dropped redundant column
- **Database Integration** — Loaded cleaned DataFrame into MySQL

---

## 🗄️ Step 2 — SQL Business Analysis (MySQL)

Key queries executed in `business_queries.sql`:

| # | Query | Insight |
|---|---|---|
| 1 | Revenue by Gender | Male: $157,890 — Female: $75,191 |
| 2 | High-Spending Discount Users | 839 customers used discounts yet spent above average |
| 3 | Top 5 Products by Rating | Gloves (3.86), Sandals (3.84), Boots (3.82) |
| 4 | Shipping Type Comparison | Express ($60.48) vs Standard ($58.46) |
| 5 | Subscribers vs Non-Subscribers | 27% subscribed, near-equal avg spend |
| 6 | Discount-Dependent Products | Hat (50%), Sneakers (49.66%), Coat (49.07%) |
| 7 | Customer Segmentation | Loyal: 3116 — Returning: 701 — New: 83 |
| 8 | Top 3 Products per Category | Jewelry, Blouse, Sandals, Jacket lead categories |
| 9 | Repeat Buyers & Subscriptions | 2518 repeat buyers are non-subscribers |
| 10 | Revenue by Age Group | Young Adult leads at $62,143 |

---

## 📈 Step 3 — Power BI Dashboard

An interactive dashboard built in Power BI featuring:

- 📌 **KPI Cards** — Total Customers (3.9K), Avg Purchase Amount ($59.76), Avg Review Rating (3.75)
- 🍩 **Subscription Status** — Donut chart (Yes 27% / No 73%)
- 📊 **Revenue & Sales by Category** — Clothing leads
- 📊 **Revenue & Sales by Age Group** — Young Adults on top
- 🔍 **Filters** — Gender, Category, Shipping Type

> Dashboard file: `Shopping_Behaviour_Analysis.pbix`

---

## 💡 Key Findings

- **Gender Revenue Gap** — Male customers generated 2.1x more revenue than female customers
- **Loyal Customers Dominate** — 80% of customers (3,116) classified as Loyal
- **Discount Paradox** — 839 high-spending discount users still exceeded average spend ($59.76)
- **Subscription Gap** — Only 27% subscribe despite nearly identical average spend to non-subscribers
- **Young Adults Lead** — Highest revenue contribution at $62,143
- **Express Shipping Upsell** — Express users spend ~$2 more on average than standard shipping users

---

## ✅ Business Recommendations

1. **Boost Subscriptions** — Introduce exclusive perks (early access, free shipping, loyalty points) to convert the 73% non-subscriber base
2. **Loyalty Programs** — Reward repeat buyers with tiered benefits to retain and grow the Loyal segment
3. **Smarter Discount Strategy** — Apply discounts selectively on high-discount items (Hat, Sneakers, Coat) while protecting margins
4. **Product Spotlight Campaigns** — Promote top-rated products (Gloves, Sandals, Boots) in targeted campaigns
5. **Demographic Targeting** — Focus higher-spend campaigns on Young Adults and Male segments

---

## 🚀 How to Run

### Python (EDA & Cleaning)
```bash
# Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# Run the notebook
jupyter notebook python/Shoping_Behaviour_Analysis.ipynb
```

### SQL (MySQL)
```bash
# Connect to your MySQL instance and run
mysql -u your_username -p your_database < sql/business_queries.sql
```

### Power BI
Open `dashboard/Shopping_Behaviour_Analysis.pbix` in **Power BI Desktop**

---

## 👨‍💻 Author

**Manoj Kumar Nishad**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?logo=linkedin)](https://www.linkedin.com/in/manojkumarnishad/)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?logo=github)](https://github.com/nsdmanoj)
[![Email](https://img.shields.io/badge/Email-Contact-D14836?logo=gmail)](mailto:nsdmanoj.13@gmail.com)

---

⭐ *If you found this project helpful, please give it a star!*
