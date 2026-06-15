# Data Quality Report

## Dataset Overview

* Rows: 255,347
* Columns: 18
* Memory Usage: 35,1 MB

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

## No Nulls values in dataset

|                |   0 |
|:---------------|----:|
| LoanID         |   0 |
| Age            |   0 |
| HasCoSigner    |   0 |
| LoanPurpose    |   0 |
| HasDependents  |   0 |
| HasMortgage    |   0 |
| MaritalStatus  |   0 |
| EmploymentType |   0 |
| Education      |   0 |
| DTIRatio       |   0 |
| LoanTerm       |   0 |
| InterestRate   |   0 |
| NumCreditLines |   0 |
| MonthsEmployed |   0 |
| CreditScore    |   0 |
| LoanAmount     |   0 |
| Income         |   0 |
| Default        |   0 |

## Dataset

The dataset contains 255,347 loan records with borrower demographics, financial information, and loan characteristics. Variables include age, income, loan amount, credit score, employment length, interest rate, and loan term.

|                |   count |          mean |          std |     min |      25% |      50% |      75% |      max |
|:---------------|--------:|--------------:|-------------:|--------:|---------:|---------:|---------:|---------:|
| Age            | 255347  | 43.4983       | 14.9903      | 18      | 31       | 43       | 56       | 69       |
| Income         | 255347  | 82499.3046    | 38963.0137   | 15000   | 48825.5  | 82466    | 116219   | 149999   |
| LoanAmount     | 255347  | 127578.8655   | 70840.7061   | 5000    | 66156    | 127556   | 188985   | 249999   |
| CreditScore    | 255347  | 574.2643      | 158.9039     | 300     | 437      | 574      | 712      | 849      |
| MonthsEmployed | 255347  | 59.5420       | 34.6434      | 0       | 30       | 60       | 90       | 119      |
| NumCreditLines | 255347  | 2.5010        | 1.1170       | 1       | 2        | 2        | 3        | 4        |
| InterestRate   | 255347  | 13.4928       | 6.6364       | 2       | 7.77     | 13.46    | 19.25    | 25       |
| LoanTerm       | 255347  | 36.0259       | 16.9693      | 12      | 24       | 36       | 48       | 60       |
| DTIRatio       | 255347  | 0.5002        | 0.2309       | 0.1     | 0.3      | 0.5      | 0.7      | 0.9      |
| Default        | 255347  | 0.1161        | 0.3204       | 0       | 0        | 0        | 0        | 1        |
