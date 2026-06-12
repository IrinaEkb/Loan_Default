# Data Quality Report

## Dataset Overview

* Rows: 255,347
* Columns: 18
* Memory Usage: 24,83 MB

---

## Data Types

| Column         | Type    |
| -------------- | ------- |
| LoanID         | object  |
| Age            | int64   |
| Income         | int64   |
| LoanAmount     | int64   |
| CreditScore    | int64   |
| MonthsEmployed | int64   |
| NumCreditLines | int64   |
| InterestRate   | float64 |
| LoanTerm       | int64   |
| DTIRatio       | float64 |
| Education      | object  |
| EmploymentType | object  |
| MaritalStatus  | object  |
| HasMortgage    | object  |
| HasDependents  | object  |
| LoanPurpose    | object  |
| HasCoSigner    | object  |
| Default        | int64   |

---

## Missing Values

No missing values were detected in any column.

---

## Duplicate Records

Duplicate rows found: 0

No duplicate records were detected.

---

## Numerical Data Summary

| Metric        | Observation     |
| ------------- | --------------- |
| Age           | 18–69 years     |
| Income        | $15,000–149,999 |
| Loan Amount   | $5,000–249,999  |
| Credit Score  | 300–849         |
| Interest Rate | 2%–25%          |
| DTI Ratio     | 0.10–0.90       |



---

## Categorical Columns

| Column         | Unique Values |
| -------------- | ------------- |
| Education      | 4             |
| EmploymentType | 4             |
| MaritalStatus  | 3             |
| HasMortgage    | 2             |
| HasDependents  | 2             |
| LoanPurpose    | 5             |
| HasCoSigner    | 2             |

LoanID contains unique identifiers for all records.

---

## Initial Assessment

The dataset appears clean and ready for exploratory data analysis.

Key findings:

* No missing values
* No duplicate records
* Data types are appropriate
* Numerical variables fall within expected ranges
* Categorical variables have low cardinality and are suitable for encoding
