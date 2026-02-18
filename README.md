# Financial-Distress-Risk-Modeling-and-Prediction-Using-Machine-Learning-on-SEC-Filings

1. Data Ingestion

Source: U.S. Securities and Exchange Commission (SEC) – EDGAR Database

Retrieve structured financial statement data via SEC EDGAR API

Parse XBRL data from:

Form 10-K (Annual Reports)

Form 10-Q (Quarterly Reports)

Extract core financial statement variables

Output: Raw firm-level financial data

2. Data Cleaning & Structuring

Normalize financial tags across companies

Handle missing values and inconsistencies

Align fiscal reporting periods

Construct a time-indexed company-year panel dataset

Output: Clean, structured firm-year dataset

3. Feature Engineering

Generate financially meaningful ratios capturing leverage, profitability, liquidity, and growth:

Debt-to-Assets Ratio

Debt-to-Equity Ratio

Return on Assets (ROA)

Net Profit Margin

Cash Flow to Liabilities

Revenue Growth Rate

Output: Feature matrix (X)

4. Label Generation

Identify financial distress or bankruptcy-related events

Create forward-looking labels (t → t+1)

Define binary classification target:

0 = Financially Healthy

1 = Financially Distressed

Output: Target variable (y)

5. Time-Aware Train/Test Split

Split data chronologically

Prevent look-ahead bias

Simulate real-world forecasting deployment

6. Model Training

Train supervised binary classification models:

Logistic Regression (baseline)

Random Forest

Gradient Boosting

XGBoost

7. Model Evaluation

Evaluate predictive performance using:

ROC-AUC

Precision

Recall

F1-Score

Precision-Recall Curve

Special consideration is given to class imbalance due to the rarity of distress events.

8. Risk Scoring System

Generate probabilistic distress scores (0–1 scale)

Classify firms into High-Risk / Low-Risk categories

Extract feature importance for interpretability

Final Output:
A deployable financial risk prediction framework capable of early-warning distress detection.

Pipeline Overview

SEC EDGAR → Data Cleaning → Feature Engineering → Labeling → Time-Aware Split → Model Training → Evaluation → Risk Scoring Output
