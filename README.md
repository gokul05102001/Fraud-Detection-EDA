
# Fraud Detection EDA Project

## Overview
This project performs **Exploratory Data Analysis (EDA)** on the `Fraud.csv` dataset provided for the Accredian assessment.  
The dataset contains 30 days of simulated transaction data, with 744 total time steps (1 hour per step).  
The primary goal is to identify transaction patterns, analyze fraud behavior, and visualize trends.

## Dataset Description

- **step**: Unit of time (1 step = 1 hour). Total: 744 steps (30 days).
- **type**: Transaction type â€” `CASH-IN`, `CASH-OUT`, `DEBIT`, `PAYMENT`, `TRANSFER`.
- **amount**: Amount of the transaction in local currency.
- **nameOrig**: Customer initiating the transaction.
- **oldbalanceOrg**: Balance before the transaction.
- **newbalanceOrig**: Balance after the transaction.
- **nameDest**: Recipient customer ID.
- **oldbalanceDest**: Recipient's balance before the transaction. (Not available for merchants â€” IDs starting with 'M').
- **newbalanceDest**: Recipient's balance after the transaction. (Not available for merchants â€” IDs starting with 'M').
- **isFraud**: Indicates transactions made by fraudulent agents in the simulation.
- **isFlaggedFraud**: Indicates flagged illegal transfers (> 200,000 in a single transaction).

## Key Analysis Performed
1. **Data Inspection**  
   - Data types, structure, missing values check.

2. **Distribution Analysis**  
   - Transaction type distribution.
   - Fraud vs Non-Fraud transaction counts.
   - Fraud rate by transaction type.

3. **Fraud Pattern Analysis**  
   - Fraudulent transaction amounts.
   - Large flagged transfers (> 200,000).

4. **Time-based Trends**  
   - Fraud cases over simulation time steps.

5. **Visualizations**  
   - Bar charts, boxplots, line graphs for fraud trends and transaction patterns.

## Requirements
To run this notebook, install the following packages:
```bash
pip install pandas matplotlib seaborn
```

## Usage
1. Place the `Fraud.csv` file in the same directory as the notebook.
2. Open `Fraud_EDA_Notebook.ipynb` in Jupyter Notebook or JupyterLab.
3. Run cells step-by-step to see both the analysis and visualizations.

## Insights
- Fraud is concentrated in specific transaction types (`TRANSFER` and `CASH-OUT`).
- Illegal flagged transactions are rare but involve high amounts.
- Fraud attempts are spread across the simulation but peak at certain hours.

---
**Author:** Gokul M  
**Purpose:** Accredian Data Science Assessment
