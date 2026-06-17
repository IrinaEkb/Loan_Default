#  Loan Default Prediction Project

## Project Goal

To analyze key factors influencing loan default risk and build a predictive model to identify high-risk borrowers.

---

##  Business Questions

- What drives loan default risk?
- How does credit score influence default probability?
- Do higher interest rates increase default risk?
- Which customer segments are the riskiest?
- Can we predict default using borrower attributes?

---

##  Dataset Description

This dataset contains borrower financial and personal attributes used to predict loan default.

## Data Quality Checks

Before analysis, the dataset was validated to ensure it is clean and reliable for modeling.

Key checks performed:

- Dataset structure: **255,347 rows × 18 columns**
- Missing values: **0 (no missing data)**
- Duplicate records: **0 (no duplicates found)**

- Numerical range validation confirmed all values are within expected limits:
  - Age: 18–69
  - Income: $15,000–$149,999
  - Loan Amount: $5,000–$249,999
  - Credit Score: 300–849
  - Loan Term: 12–60 months

- Binary categorical variables (`Yes/No`) were converted into numeric format (`0/1`) for analysis and modeling

- Data distributions were reviewed to ensure consistency and detect anomalies

Overall result:
- No missing values
- No duplicates
- No invalid or out-of-range records

📄 Full Data Quality Report: [Data Quality Report](reports/data_quality_report.md)

---

## Exploratory Data Analysis (EDA)

EDA was conducted to identify key drivers of loan default risk and understand borrower behavior.

Main analyses included:

- Correlation analysis between features and default:
  - strongest positive relationship: Interest Rate (**+0.131**)
  - strongest negative relationship: Age (**-0.168**)

- Default rate by employment type:
  - unemployed: **13.6%**
  - part-time/self-employed: **~11–12%**
  - full-time: **9.5%**

- Credit score analysis:
  - low score group: **~13.7% default rate**
  - high score group: **~9.8% default rate**
  - weak separation effect overall

- Income segmentation:
  - low income borrowers: **~22.5% default rate**
  - high income borrowers: **~8.8% default rate**
  - strong downward trend with increasing income

- Loan amount comparison:
  - defaulted borrowers: **$144,515 average**
  - non-defaulted borrowers: **$125,354 average**

- Overall default rate:
  - **11.61% (≈1 in 9 borrowers)**

- Group comparisons:
  - Defaulted borrowers tend to have lower income, higher loan amounts, and slightly lower credit scores

- Key risk drivers:
  - interest rate
  - income level
  - loan amount
  - employment stability

### Example Visualization

![Top Risk Factors](visuals/top_risk_factors.png)

📄 Full EDA Report: [EDA Report](reports/eda_report.md)