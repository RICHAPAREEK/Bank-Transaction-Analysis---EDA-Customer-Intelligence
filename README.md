# 🏦 Bank Transaction Analysis — Extended EDA & Customer Intelligence

> **End-to-end Python analytics project** on 5,000 bank transactions — covering spending patterns, cohort retention, RFM segmentation, churn detection, and campaign targeting.

---

## 📌 Project Overview

This project performs comprehensive analysis of bank transaction data, simulating the kind of work done in real banking and fintech analytics teams. It goes beyond basic EDA to include customer lifecycle analysis, behavioral segmentation, and retention intelligence.

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3 | Core language |
| Pandas | Data wrangling & aggregation |
| NumPy | Numerical operations |
| Matplotlib | Charts & visualizations |
| Seaborn | Heatmaps & statistical plots |
| Jupyter Notebook | Development environment |

---

## 📂 Datasets

Three CSV files merged into one unified dataframe:

| File | Description |
|------|-------------|
| `customers.csv` | Demographics — age, city, account type |
| `accounts.csv` | Account details and balance |
| `transactions.csv` | 5,000 records — date, amount, merchant, type |

---

## 📊 Analysis Sections

### 🔹 Section 1 — EDA & Business Insights
- Merged 3 datasets; data type conversion and cleaning
- Feature engineering: `month`, `month_num` from date
- Top 10 customers by total spend
- City-wise revenue breakdown
- Monthly transaction trend (line chart)
- Transaction amount distribution (histogram + KDE)
- Fraud detection — flagged transactions above Rs.1,00,000

### 🔹 Section 2 — Spending Patterns & User Behavior
- Top 10 merchants by total spend
- Credit vs Debit spending split (pie chart)
- Spending by account type — total, average, count
- Age group segmentation using pd.cut() → (<25, 25-35, 35-45, 45-60, 60+)
- Day-of-week spending pattern — peak transaction days

### 🔹 Section 3 — Cohort & Time-Based Analysis
- Cohort defined by customer's first transaction month
- period_number = months since joining
- Cohort retention matrix via pivot table
- Retention % relative to Month 0 (cohort size)
- Seaborn heatmap for visual retention analysis
- Monthly Active Users (MAU) trend
- Monthly revenue trend with chronological sorting via pd.Categorical

### 🔹 Section 4 — RFM Analysis (Customer Segmentation)
- Recency — days since last transaction
- Frequency — total transaction count per customer
- Monetary — total spend per customer
- Each scored 1-3 using pd.qcut() quantile binning
- RFM Total Score: min=3, max=9
- Segments: High Value (8-9), Mid Value (5-7), Low Value (3-4)

### 🔹 Section 5 — Churn Detection & Retention
- Churn defined as: recency > 90 days
- Churn rate calculated using boolean mean
- Active vs Churned pie chart
- City-wise retention rate ranking
- Campaign Targeting Lists (available in notebook):
  - Win-Back — churned High/Mid Value customers
  - Loyalty Reward — active High Value customers
  - Upsell — active Mid Value customers

---

## 💡 Key Business Insights

- Identified top revenue customers and highest-earning cities for targeted outreach
- Flagged high-value outlier transactions (>Rs.1,00,000) for fraud review
- Cohort heatmap revealed significant customer drop-off after Month 1
- RFM model produced clear High/Mid/Low value segments for differential marketing
- Churn analysis identified at-risk customers enabling proactive retention campaigns
- City-wise retention rates surfaced locations needing immediate re-engagement strategy

---

## 🚀 How to Run

```bash
# 1. Clone the repository
git clone https://github.com/your-username/bank-transaction-analysis.git
cd bank-transaction-analysis

# 2. Install dependencies
pip install pandas numpy matplotlib seaborn jupyter

# 3. Add datasets to project folder
#    customers.csv | accounts.csv | transactions.csv

# 4. Launch notebook
jupyter notebook Bank_Analysis_Extended.ipynb

# 5. Run: Kernel > Restart & Run All
```

---

## 📁 Project Structure

```
bank-transaction-analysis/
│
├── Bank_Analysis_Extended.ipynb   <- Main analysis notebook
├── customers.csv                  <- Customer demographics
├── accounts.csv                   <- Account data
├── transactions.csv               <- Transaction records
└── README.md                      <- Project documentation
```

---

## 📝 Note

Some advanced sections are available in the notebook as commented code:
- High-Value Customer Profile (Top 10% by spend) — Cell 35
- Campaign Audience Size Summary — Cell 42

These can be uncommented and run independently without affecting other sections.

---

## 👩 Author

**Richa Pareek** — Data Analyst | Python · SAS · Power BI · SQL
pareekriya43@gmail.com | LinkedIn | GitHub
