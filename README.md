# Project Overview

This project explores Instacart customer purchasing behavior using Python. The analysis covers data cleaning, feature engineering, and exploratory visualizations to uncover patterns in customer loyalty, spending habits, and demographics. Using Pandas, Matplotlib, and Seaborn, the project identifies key customer profiles (e.g., Established Families, Young Adults, Mature Affluent) and their ordering habits across regions and product departments. The results help inform marketing and sales strategies for customer targeting and retention.

## Project goals

Instacart wanted to better understand how customers shop, specifically when they order, how much they spend, what departments drive demand, and whether behaviors differ by loyalty, region, or demographic segments.

Key objectives included:
- Identify busiest days and hours for ordering (ad scheduling)
- Determine peak spending times (product placement and promo timing)
- Reveal most-ordered departments
- Compare ordering habits by loyalty, region, and demographics
- Build customer profiles using age, income, and purchasing patterns

---

## Dataset

- **Primary data:** Instacart Online Grocery Dataset (Kaggle)
- **Supplemental data:** Fabricated customer demographics (CareerFoundry)
- **Scale:** ~3M rows across six source files, merged into one analysis-ready DataFrame

Note: This is an educational portfolio project and is not affiliated with Instacart.

---

## Tools used

- Python (Pandas, NumPy)
- Matplotlib, Seaborn (visualizations)
- Jupyter Notebook
- Excel (stakeholder summary/reporting)

---

## Approach

High-level workflow:
1. **Data preparation:** consistency checks, missing values, duplicates, standardized naming, data types
2. **Feature engineering:** created segmentation and behavior flags (examples below)
3. **Visual analysis:** built a set of charts aligned to business questions
4. **Stakeholder reporting:** exported charts and summarized insights in Excel

Example engineered fields include:
- `loyalty_flag`
- `avg_order_spending_flag`
- `region`
- `customer_profile`

Customer profiles used in the analysis included **Young Parent**, **Established Family**, **Mature Affluent**, **Young Adult**, and **General Shopper**.

---

## Key findings (highlights)

- **Busiest times:** Orders peak between **8 AM and 4 PM**
- **Top departments:** **Produce** and **Dairy & Eggs** dominate order activity
- **Regional patterns:** Spending behavior is broadly consistent across U.S. regions
- **Customer profiles:** Ordering behavior differences exist, but overall variation by profile is modest in this dataset

---

## Recommendations (from the analysis)

1. Optimize ad timing by targeting early morning and evening hours (outside the 8 AM–4 PM peak window)
2. Keep Produce and Dairy central to marketing, and cross-promote lower-volume departments
3. Tailor messaging: household value for families, digital convenience for younger audiences
4. Strengthen loyalty with rewards and personalization
5. Maintain cohesive national campaigns, while monitoring subtle shifts over time

---

## Repository structure

- `Scripts/`  
  Jupyter notebooks for cleaning, merging, feature engineering, aggregation, and visualization work.

- `Analysis/Visualizations/`  
  Saved charts and exported visuals.

- `Deliverables/`  
  Stakeholder-facing exports (Excel summary/report).

- `Project Management/`  
  Project planning and supporting documentation.

---

## How to run locally

Because the raw dataset is large and often not committed to GitHub, the typical setup is:
1. Clone the repo
2. Download the Instacart dataset (Kaggle) and place the CSVs in a local `data/` directory (or wherever your notebooks expect them)
3. Create a virtual environment and install dependencies
4. Run notebooks in `Scripts/`

Example (macOS / Linux):

```bash
git clone https://github.com/stephenhelvig/instacart-python.git
cd instacart-python

python3 -m venv .venv
source .venv/bin/activate

pip install pandas numpy matplotlib seaborn jupyter
jupyter notebook
