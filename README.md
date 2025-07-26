# Wallet Risk Scoring System

A DeFi credit scoring system that analyzes on-chain wallet behavior from the Compound V2 protocol and assigns a **risk score from 0 to 1000**. This system helps in identifying trustworthy vs. high-risk wallets based on real transaction data.

## Overview

This project demonstrates:
- Fetching wallet activity on Compound V2 protocol
- Feature engineering from transaction logs
- Risk-based scoring system
- Exploratory analysis of wallet behaviors

## Methodology

### Feature Engineering:
- Borrow Count
- Repayment Ratio
- Liquidation Events
- Net Borrowed Amount
- Time-based activity patterns

### Scoring:
Each wallet is scored on a scale of 0–1000 based on the above features using a weighted heuristic system.

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


