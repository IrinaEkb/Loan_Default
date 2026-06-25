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

