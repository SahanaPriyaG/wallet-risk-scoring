# Wallet Risk Scoring System

A DeFi credit scoring system that analyzes on-chain wallet behavior from the Compound V2 protocol and assigns a **risk score from 0 to 1000**. This system helps in identifying trustworthy vs. high-risk wallets based on real transaction data.

## Overview

This project demonstrates:
- Fetching wallet activity on Compound V2 protocol
- Feature engineering from transaction logs
- Risk-based scoring system
- Exploratory analysis of wallet behaviors

---

## Methodology

| Step | Description |
|------|-------------|
| 1️ | **Data Collection** from Compound V2 via APIs (mocked or simulated for this demo). |
| 2️ | **Feature Engineering** including repayment count, borrow-repay ratio, liquidation count, etc. |
| 3️ | **Risk Scoring** using normalized features and weighted scoring logic. |
| 4️ | **Score Bucketing** from 0 to 1000 into risk categories. |
| 5️ | **Visualization & Export** via graphs and CSV output. |

---

##  Features Considered

| Feature                | Purpose                               |
|------------------------|----------------------------------------|
| Repayment Count        | Higher = lower risk                   |
| Borrow-to-Repay Ratio  | Lower = better risk profile           |
| Liquidation Count      | Higher = higher risk                  |
| Unique Assets Used     | Indicates diversification             |
| Activity Span (Days)   | Longer activity = more reliable       |

---

## Risk Scoring Logic

| Feature                | Weight (%) |
|------------------------|------------|
| Repayment Count        | 25%        |
| Borrow-to-Repay Ratio  | 20%        |
| Liquidation Count      | -25%       |
| Unique Assets Used     | 10%        |
| Activity Span (Days)   | 20%        |

---

## Visualizations

- Risk Score Distribution
- Risk Bucket Histogram
- Feature Correlation Heatmap
---

## Files Included

| File | Description |
|------|-------------|
| `main_notebook.ipynb` | Full code |
| `wallet_scores_Output......csv` | Wallet ID with computed scores |
| `analysis.md` | Score bucket breakdown & behavior insights |
| `README.md` | Project overview and method |

## Output

![Score Distribution](wallet_scores_Output......csv)

## Score Buckets

| Score Range | Description |
|-------------|-------------|
| 0–100       | Extremely risky: many liquidations |
| 101–200     | Early warning signs, irregular repayments |
| 201–400     | Low usage, minor risk |
| 401–600     | Average behavior, reliable |
| 601–800     | Good usage, consistent |
| 801–1000    | Excellent behavior, zero liquidations |

##  Dependencies

pandas
numpy
matplotlib
seaborn


