# Loan Size Strategy for High-Risk Borrowers

## Business Problem

The current loan portfolio has a default rate of approximately 11.6%.

Exploratory analysis shows that defaulted borrowers tend to have:

* Lower income
* Larger loan balances
* Higher repayment pressure

In particular, low-income borrowers exhibit substantially higher default rates than the rest of the portfolio.

Management is considering a policy that limits maximum loan amounts for financially vulnerable borrowers.

---

## Business Question

What is the potential financial impact of introducing loan size caps for low-income borrowers?

Specifically:

* How much larger are loans issued to defaulted borrowers?
* How much loan exposure is concentrated in low-income segments?
* How many dollars of high-risk lending could potentially be avoided?
* Could reducing loan sizes improve portfolio quality without significantly reducing lending volume?

---

## Hypothesis

Low-income borrowers are not defaulting because of loan term length.

Instead, they appear to be borrowing amounts that are disproportionately large relative to their income.

If loan amounts are reduced for these borrowers, repayment burden may decrease and portfolio losses may be reduced.

---

## Analytical Approach

1. Identify low-income borrower segments.
2. Measure average loan amounts by income group.
3. Compare loan sizes between repaid and defaulted borrowers.
4. Estimate total loan exposure issued to high-risk income groups.
5. Simulate a loan cap policy and evaluate the reduction in portfolio risk.

## Loan Term Analysis

| Loan Term | Default Rate (%) |
|-----------|-----------------:|
| 12 months | 11.62 |
| 24 months | 11.61 |
| 36 months | 11.57 |
| 48 months | 11.57 |
| 60 months | 11.70 |

Default rates remain almost identical across all loan terms (approximately 11.6%).

This suggests that extending or shortening loan maturity alone is unlikely to materially reduce default risk.

## Defaulted Borrowers by Loan Term

| Loan Term | Borrowers | Avg Income | Avg Loan | Avg Credit Score |
|-----------|----------:|-----------:|----------:|-----------------:|
| 12 | 5,920 | 71,763 | 145,101 | 557.80 |
| 24 | 5,921 | 72,344 | 144,290 | 560.94 |
| 36 | 5,907 | 71,250 | 145,529 | 560.64 |
| 48 | 5,922 | 71,782 | 143,853 | 561.85 |
| 60 | 5,983 | 72,081 | 143,814 | 555.25 |

Defaulted borrowers look nearly identical across all loan terms.

Average income, loan amount and credit score vary only slightly, providing little evidence that loan maturity itself explains default behavior.

## Risk by Income Segment

| Income Segment | Borrowers | Avg Loan | Avg Predicted PD | Actual Default Rate |
|---------------|----------:|----------:|-----------------:|--------------------:|
| Low | 63,837 | 127,624 | 17.66% | 17.38% |
| Medium | 63,837 | 127,714 | 11.08% | 10.54% |
| High | 63,839 | 127,344 | 9.50% | 9.51% |
| Very High | 63,834 | 127,633 | 8.78% | 9.02% |

Loan amounts are almost identical across all income groups.

However, default probability decreases substantially as income increases.

This suggests that borrower income—not loan term or average loan size—is the strongest driver of portfolio risk.

## Loan Term Analysis

| Loan Term | Default Rate (%) |
|-----------|-----------------:|
| 12 months | 11.62 |
| 24 months | 11.61 |
| 36 months | 11.57 |
| 48 months | 11.57 |
| 60 months | 11.70 |

Default rates remain stable across all loan terms (~11.6%).

There is no meaningful variation in risk across different maturities, which indicates that loan term structure does not materially influence default behavior.

---

## Borrower Profile by Loan Term

| Loan Term | Borrowers | Avg Income | Avg Loan | Avg Credit Score |
|-----------|----------:|-----------:|----------:|-----------------:|
| 12 | 5,920 | 71,763 | 145,101 | 557.80 |
| 24 | 5,921 | 72,344 | 144,290 | 560.94 |
| 36 | 5,907 | 71,250 | 145,529 | 560.64 |
| 48 | 5,922 | 71,782 | 143,853 | 561.85 |
| 60 | 5,983 | 72,081 | 143,814 | 555.25 |

Borrower characteristics remain stable across all loan terms.

No structural differences are observed in income levels, loan size, or credit scores.

---

## Income vs Risk Distribution

| Income Segment | Borrowers | Avg Loan | Avg Predicted PD | Default Rate |
|---------------|----------:|----------:|-----------------:|-------------:|
| Low | 63,837 | 127,624 | 17.66% | 17.38% |
| Medium | 63,837 | 127,714 | 11.08% | 10.54% |
| High | 63,839 | 127,344 | 9.50% | 9.51% |
| Very High | 63,834 | 127,633 | 8.78% | 9.02% |

Default risk decreases significantly with income level.

Loan amounts remain almost identical across all income groups, meaning risk differences are not driven by loan size but by borrower financial capacity.

---

## Low-Income Segment Exposure

| Metric | Value |
|--------|------:|
| Borrowers | 63,837 |
| Average Loan | $127,624 |
| Standard Deviation | $70,711 |
| Median | $127,810 |
| Maximum | $249,993 |
| Average Default Probability | 17.66% |

Low-income borrowers represent a large, high-risk portion of the portfolio.

---

# Strategy 1: 10% Loan Cap (Low-Income Segment)

## Exposure Impact

| Metric | Value |
|--------|------:|
| Current Exposure | $8,147,165,148 |
| New Exposure | $7,332,448,633 |
| Exposure Reduction | $814,716,515 |

## Expected Loss Impact

| Metric | Value |
|--------|------:|
| Current Expected Loss | $1,732,430,116 |
| New Expected Loss | $1,559,187,104 |
| Expected Loss Reduction | $173,243,012 |
| Efficiency (Loss / Exposure Reduction) | 21.3% |

## Loan Size Effect

| Metric | Value |
|--------|------:|
| Average Loan (Before) | $127,624 |
| Average Loan (After) | $114,862 |
| Reduction per Borrower | $12,762 |

Loan reduction lowers both exposure and expected losses proportionally, while preserving portfolio structure.

---

# Strategy 2: High-Risk Segment (Income + Credit Score + DTI Filter)

## Segment Definition

- Income Segment: Low  
- Credit Score < 350  
- DTI Ratio > 0.60  

---

## High-Risk Segment Profile

| Metric | Value |
|--------|------:|
| Borrowers | 2,109 |
| Average Income | $32,256 |
| Average Loan | $127,224 |
| Average Credit Score | 325 |
| Average DTI | 0.75 |
| Average Predicted Default Probability | 21.75% |
| Observed Default Rate | 20.63% |
| Total Exposure | $268,315,030 |

This segment represents a concentrated high-risk pool with elevated default probability.

---

# Strategy 2A: 10% Loan Cap (High-Risk Segment)

## Impact

| Metric | Value |
|--------|------:|
| Exposure Reduction | $26,831,503 |
| Expected Loss Reduction | $6,743,140 |
| Efficiency | 25.1% |

---

# Strategy 2B: 20% Loan Cap (High-Risk Segment)

## Impact

| Metric | Value |
|--------|------:|
| Exposure Reduction | $53,663,006 |
| Expected Loss Reduction | $13,486,281 |
| Efficiency | 25.1% |

Stricter caps increase absolute impact while maintaining stable efficiency.

---

# Final Conclusion

## Answer to Business Questions

### 1. How much larger are loans issued to defaulted borrowers?

Defaulted borrowers consistently receive large and uniform loan amounts across segments:

- Average loan size (defaulted borrowers): **~$143K–$145K**
- Income groups show almost identical loan sizes:
  - Low income: $127,624
  - Medium income: $127,714
  - High income: $127,344

Difference in loan size between risk groups is negligible (<1%), meaning loan amount is not currently risk-adjusted.

---

### 2. How much loan exposure is concentrated in low-income segments?

Low-income segment represents the largest risk exposure layer:

- Number of borrowers: **63,837**
- Total exposure: **$8.15B**
- Share of portfolio: ~**100% within modeled segment baseline**
- Average default probability: **17.66%**

This segment alone drives a significant portion of expected portfolio losses:

- Expected loss (baseline): **$1.73B**

---

### 3. How many dollars of high-risk lending could be avoided?

#### Strategy 1: 10% cap (low-income borrowers)

- Exposure reduction: **$814.7M**
- Expected loss reduction: **$173.2M**
- Efficiency: **21.3 cents loss reduction per $1 reduced lending**

---

#### Strategy 2A: High-risk segment (10% cap)

(high income + low score + high DTI)

- Exposure reduction: **$26.8M**
- Expected loss reduction: **$6.74M**
- Efficiency: **25.1%**

---

#### Strategy 2B: High-risk segment (20% cap)

- Exposure reduction: **$53.7M**
- Expected loss reduction: **$13.5M**
- Efficiency: **25.1%**

---

### Total avoided high-risk lending (combined view)

- Conservative policy (10% low-income cap): **$814.7M exposure reduction**
- Targeted high-risk tightening: **up to $53.7M additional reduction**
- Total potential controllable exposure: **~$868M**

---

### 4. Could reducing loan sizes improve portfolio quality without significantly reducing lending volume?

#### Portfolio impact summary

| Scenario | Exposure Reduced | Expected Loss Reduced | Efficiency |
|----------|----------------:|---------------------:|-----------:|
| Low-income -10% | $814.7M | $173.2M | 21.3% |
| High-risk -10% | $26.8M | $6.7M | 25.1% |
| High-risk -20% | $53.7M | $13.5M | 25.1% |

---

## Strategy Comparison

### Key finding across all simulations

- Exposure reduction scales linearly with loan caps
- Expected loss reduction is proportional to exposure reduction
- Efficiency remains stable between **21%–25%**

---

## Recommended Strategy

### Best risk-adjusted policy: Hybrid approach

Combine both segments:

- Apply **10% cap to low-income borrowers**
- Apply **20% cap to high-risk (Low Income + Credit Score < 350 + DTI > 0.60)**

### Expected combined impact:

- Exposure reduction: **~$868M**
- Expected loss reduction: **~$179M**
- Loss-to-exposure efficiency: **~21–25%**

---

## Business Interpretation

### Risk reduction achieved:

- Significant reduction in high-risk exposure: **$800M+**
- Meaningful reduction in expected portfolio losses: **$170M–$180M**
- Risk reduction is stable and predictable across scenarios

### Revenue trade-off:

- Lending volume decreases proportionally with caps
- No evidence of disproportionate loss in efficiency
- Risk reduction is directly controllable via policy strength

---

## Final Answer to Business Question

Introducing loan size caps leads to:

- **$814M–$868M reduction in risky exposure**
- **$173M–$179M reduction in expected losses**
- Stable efficiency of **~21–25% risk reduction per dollar of lending removed**

Loan caps improve portfolio risk profile, but reduce total lending volume linearly.

The optimal configuration is a **targeted hybrid cap strategy**, where higher restrictions are applied only to structurally high-risk borrowers rather than the entire low-income segment.