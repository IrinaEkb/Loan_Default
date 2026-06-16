# Exploratory Data Analysis (EDA) Report: Credit Risk Factors

---

## 1. Target Variable Analysis (Class Imbalance)

```python
df['Default'].value_counts(normalize=True)
# False (0): 0.883872
# True  (1): 0.116128
```

### Key Findings:
* **Imbalance:** 88.4% of clients are non-default, while 11.6% defaulted.
* **Modeling Impact:** Metric selection must prioritize Precision, Recall, and F1-score. Standard Accuracy will yield misleadingly high performance due to the dominant class.

---
