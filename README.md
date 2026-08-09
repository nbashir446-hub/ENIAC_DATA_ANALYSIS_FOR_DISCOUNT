# ENIAC_DATA_ANALYSIS_FOR_DISCOUNT
Data analysis project evaluating the financial impact, performance, and strategic effectiveness of product discounts for the ENIAC e-commerce platform using Python and pandas.
# Eniac E-Commerce: Discount Strategy & Revenue Performance Evaluation

## 📌 Project Overview
The objective of this project is to settle an ongoing strategic debate within Eniac's leadership team regarding the financial impact of its permanent discount model. 

* **The Marketing Team** argues that aggressive discounting drives customer acquisition, improves satisfaction, and secures long-term market expansion.
* **The Board of Investors** is deeply concerned with margin erosion, pointing out that while recent quarterly order volumes increased, total net revenue dropped. 

By executing an end-to-end data analysis on transactional data (2017–2018), this project assesses discount efficiency, identifies margin leakage, and uncovers the "sweet spot" for pricing optimization.

## 📊 Key Business Insights & Findings

1. **The "Default Discount" Trap**
   Analysis shows that markdowns have shifted from a tactical sales lever to a permanent state, with over **90%** of order lines containing a discount. This systemic price-cutting risks diluting brand equity.

2. **Identifying the "Sweet Spot"**
   Through revenue-uplift scenario modeling, we identified an **Optimal Revenue Zone**. Net revenue peaks at a moderate discount depth of **20% to 25%**. Pushing discounts beyond 30% yields diminishing transactional volume returns while causing sharp profit margin declines.

3. **Seasonality Over Elasticity**
   Sales spikes are highly synchronized with major holiday events (e.g., Black Friday, Cyber Monday, and Q4 holidays) rather than the discount depth itself. Outside of peak seasonal windows, the correlation between discount size and daily revenue remains weak.


## 🛠️ Tech Stack & Methodology
* **Language:** Python
* **Libraries:** Pandas, NumPy, Matplotlib, Seaborn
* **Analytics Framework:** ETL (Data Extraction, Cleaning, and Transformation), Time-Series Analysis, Correlation Matrix, Scenario Modeling
* **Domain:** E-commerce / Revenue Management


## 💾 Dataset Structure
The analytical pipeline evaluates four core relational data files:
* `orders.csv`: Order IDs, creation timestamps, totals paid, and transaction fulfillment states (Completed, Pending, Cancelled).
* `orderlines.csv`: Individual line-item details linking orders to specific SKUs, quantities purchased, and unit prices.
* `products.csv`: Standard base prices, promotional pricing, stock availability, and type classifications.
* `brands.csv`: Mapping keys linking product SKU prefixes to full brand names (e.g., Apple hardware).

### Data Preprocessing & Cleaning Highlights
* **Referential Integrity:** Validated strict alignment across `products.price`, `orderlines.unit_price`, and `orders.total_paid`.
* **Data Corruption:** Handled corrupted price entries (e.g., strings with double decimals or missing values) through localized statistical imputation or targeted row drops.
* **Outliers:** Handled distribution skews using Interquartile Range (IQR) box-plot filtering to ensure metrics accurately reflect true customer behaviors.


## 📂 Repository Structure
```text
eniac-discount-analysis/
│
├── data/
│   ├── raw/               # Contains initial source CSV files
│   └── processed/         # Cleaned, Quality Data ready-for-analysis CSVs
│
├── notebooks/
│   └── ENIAC_DISCOUNT_Analysis_FILE_1.ipynb   # Complete data cleaning & analysis notebook
│   └── ENIAC_DISCOUNT_Analysis_FILE_2.ipynb

├── deliverables/
│   └── eniac_strategy_presentation.pdf # 5-minute executive presentation slides
│
└── README.md              # Project documentation
