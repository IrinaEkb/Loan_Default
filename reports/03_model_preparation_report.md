## 03_model_preparation.ipynb — Model Results Summary

### Data preparation
- Removed `LoanID`
- Defined features (X) and target (y = Default)
- Applied one-hot encoding to categorical variables:
  - Education
  - EmploymentType
  - MaritalStatus
  - LoanPurpose
- Train/test split:
  - Train: 80%
  - Test: 20%
  - Stratified sampling preserved default rate (~11.6%)

---

## Model
- Logistic Regression
- Threshold = 0.3

---

## Metrics

| Metric | Value |
|--------|------|
| Accuracy | 0.78 |
| ROC-AUC | 0.747 |

---

## Classification Report

| Class | Precision | Recall | F1-score | Support |
|------|----------|--------|----------|---------|
| 0 | 0.93 | 0.81 | 0.87 | 45139 |
| 1 | 0.27 | 0.52 | 0.36 | 5931 |

---

## Confusion Matrix

|  | Predicted 0 | Predicted 1 |
|--|------------|-------------|
| Actual 0 | 36725 | 8414 |
| Actual 1 | 2834 | 3097 |

---

## Key Result
- Recall for defaults: 0.52
- 48% of default cases are missed
- Model performance is limited by class imbalance