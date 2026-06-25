## 03_model_preparation.ipynb — Model Results Summary 

---

## Data Preparation

- Removed identifier column: `LoanID`
- Defined target variable:
  - `Default = 1` → client defaulted (bad loan)
  - `Default = 0` → client repaid loan (good loan)

- Feature engineering (risk signals were enhanced using domain logic):
  - Income-to-loan ratio (repayment capacity)
  - Debt burden (leverage level)
  - Score pressure (credit score vs loan size)
  - Interest rate × DTI interaction (risk intensity)
  - Combined risk score (pricing + debt burden)

- Categorical variables encoded using one-hot encoding:
  - Education
  - Employment Type
  - Marital Status
  - Loan Purpose

- Train/test split:
  - Training set: 80%
  - Test set: 20%
  - Stratification preserved default rate (~11.6%)

---

## Model

- Algorithm: Logistic Regression
- Output: Probability of default
- Decision rule: threshold-based classification

---

## Business Output (Portfolio Simulation)

| Metric | Value | Interpretation |
|--------|--------:|----------------|
| Total Profit | $166,407,402 | Net simulated profit from loan portfolio |
| Test Loan Volume | $6,526,671,409 | Total exposure evaluated on test set |
| ROI | 2.55% | Return generated per dollar of issued credit |

---

## Threshold Analysis (Profit Optimization)

### Profit vs Threshold Visualization

![Profit vs Threshold](./visuals/profit_threshold.png)

Model performance varies depending on approval strictness:

| Threshold | Profit | Business Interpretation |
|-----------|--------:|------------------------|
| 0.2 | $166.4M | Aggressive lending (high approvals) |
| 0.3 | $122.6M | Growth-focused strategy |
| 0.4 | $84.9M | Balanced risk-taking |
| 0.5 | $57.0M | Conservative lending |
| 0.6 | $41.7M | Strict approval policy |
| 0.7 | $31.6M | Very strict lending |
| 0.8 | $25.6M | Extremely conservative |

➡️ Optimal threshold under current assumptions: **0.2 (maximum profit)**

---

## Model Performance at Threshold = 0.2

### Confusion Matrix

![Confusion Matrix](./visuals/confusion_matrix.png)

|                        | Predicted Good | Predicted Default |
|------------------------|----------------|------------------|
| Good Clients           | 39,234 | 5,905 |
| Default Clients        | 3,307 | 2,624 |

---

### Interpretation

- 39,234 → safe loans correctly approved  
- 5,905 → good clients rejected  
- 3,307 → risky clients approved (credit risk)  
- 2,624 → risky clients correctly rejected  

---

Total loans:
39,234 + 5,905 + 3,307 + 2,624 = 51,070

Approved loans:
39,234 + 3,307 = 42,541

Approval rate:
42,541 / 51,070 = 0.833 → ~83%

Rejected loans:
5,905 + 2,624 = 8,529

Risk in approved portfolio:
3,307 / 42,541 = 0.0778 → ~7.8%


---

### Metrics

| Metric | Good Clients (0) | Default Clients (1) |
|--------|------------------:|--------------------:|
| Precision | 0.89 | 0.68 |
| Recall | 1.00 | 0.03 |
| F1-score | 0.94 | 0.06 |

- Recall 0.03 → model detects only 3% of defaulters  
- Precision 0.68 → when model flags risk, it is usually correct  

---

### Model Quality

| Metric | Value |
|--------|------:|
| Accuracy | 0.8858 |
| ROC-AUC | 0.751 |

---

### Comparison to previous portfolio

- Earlier default rate ≈ 11.6% (higher natural risk in dataset)
- Current model approved portfolio has ~7.8% risk exposure
- Approval rate increased to ~83%, meaning more loans are issued while risk is c

---

## Key Business Insights

- The model is **very conservative in risk detection**
  - Only **183 defaulters were correctly identified**
  - Majority of bad loans are still approved (5,748 FN)

- Very low false rejection rate:
  - Only **85 good clients were rejected**

- Profit is highly sensitive to threshold:
  - Lower threshold → higher approvals → higher profit
  - Higher threshold → fewer approvals → lower profit

- Current optimal strategy (based on simulation):
  - **Aggressive lending policy (threshold ≈ 0.2)** maximizes profit under current assumptions

---

## Final Interpretation

This model demonstrates that:

- Credit risk modeling is not only about accuracy or ROC-AUC
- Business profit depends heavily on **decision threshold selection**
- Trade-off exists between:
  - Risk reduction (catching defaulters)
  - Revenue growth (approving good clients)

