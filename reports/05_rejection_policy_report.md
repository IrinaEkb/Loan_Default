# High-Risk Borrower Rejection Strategy

## Business Problem

The current loan portfolio has an overall default rate of **11.61%**, resulting in an expected portfolio loss of approximately **$4.29 billion**.

Exploratory analysis identified a small segment of borrowers with a combination of multiple adverse risk characteristics:

- Credit Score below **400**
- Income in the lowest **25%** of the portfolio
- Debt-to-Income Ratio above **55%**

Although this segment represents only a small portion of the overall portfolio, it exhibits a substantially higher default rate than the portfolio average.

Management is evaluating whether declining applications from this highest-risk segment would improve portfolio quality and reduce expected credit losses.

---

# Business Question

What would be the financial impact of rejecting applications from borrowers that simultaneously exhibit:

- Very low credit scores
- Low income
- High debt burden

Specifically:

- How many applications would be rejected?
- How much lending volume would be removed?
- How would the overall portfolio default rate change?
- How much expected portfolio loss could be avoided?
- Is the reduction in lending volume justified by the reduction in credit risk?

---

# Rejection Policy

Reject loan applications meeting all three conditions:

| Risk Indicator | Threshold |
|---------------|-----------|
| Credit Score | < 400 |
| Income | Bottom 25% of portfolio |
| Debt-to-Income Ratio | > 55% |

This represents a highly targeted underwriting policy intended to eliminate only the most financially vulnerable applicants rather than broadly tightening lending standards.

---

# High-Risk Segment Profile

| Metric | Value |
|---------|------:|
| Rejected Applications | 5,071 |
| Default Rate | 20.19% |
| Loan Volume | $645,561,822 |
| Expected Default Loss | $159,711,094 |

### Interpretation

The identified segment represents only a small fraction of the overall portfolio but demonstrates a default rate nearly **twice the portfolio average**.

This indicates that the policy is focused on a concentrated pocket of elevated credit risk rather than broadly reducing loan originations.

---

# Portfolio Impact

## Portfolio Before Policy

| Metric | Value |
|---------|------:|
| Portfolio Volume | $32,576,880,572 |
| Portfolio Default Rate | 11.61% |
| Expected Portfolio Loss | $4,285,312,531 |

---

## Portfolio After Policy

| Metric | Value |
|---------|------:|
| Portfolio Volume | $31,931,318,750 |
| Portfolio Default Rate | 11.44% |
| Expected Portfolio Loss | $4,125,601,437 |

---

# Portfolio Changes

| Metric | Change |
|---------|-------:|
| Rejected Applications | 5,071 |
| Lending Volume Removed | $645,561,822 |
| Default Rate Improvement | -0.17 percentage points |
| Expected Loss Reduction | $159,711,094 |
| Reduction in Expected Portfolio Loss | 3.73% |

![Portfolio Policy Impact](./visuals/portfolio_policy_impact.png)

---

# Business Interpretation

At first glance, the reduction in portfolio default rate appears modest, decreasing from **11.61% to 11.44%**.

This is expected because the rejection policy affects only a relatively small subset of the overall portfolio. The vast majority of borrowers remain unchanged, so the aggregate default rate naturally moves only slightly.

However, default rate measures **the proportion of borrowers who default**, regardless of loan size.

Expected portfolio loss measures **the amount of capital exposed to default**.

These metrics capture different aspects of portfolio performance.

Although the rejected segment represents a limited share of applications, it accounts for approximately **$160 million** in expected credit losses.

As a result, a relatively small change in portfolio default rate translates into a meaningful reduction in expected financial losses.

From a portfolio management perspective, reducing expected losses is often a more important objective than maximizing improvements in default rate alone, since credit losses directly affect profitability, capital requirements, and risk-adjusted returns.

---

# Risk–Return Trade-off

The proposed policy removes approximately:

- **$646 million** of lending volume
- **5,071** loan applications

In exchange, the institution avoids approximately:

- **$160 million** in expected default losses

This illustrates a common trade-off in credit risk management.

Rejecting high-risk borrowers reduces potential revenue because fewer loans are originated.

At the same time, it reduces future credit losses by eliminating exposures with disproportionately high default risk.

The objective is not to maximize loan volume, but to improve the overall quality and profitability of the lending portfolio.

---

# Business Benefits

The proposed rejection policy provides several benefits:

- Concentrates lending on stronger borrowers.
- Reduces exposure to the highest-risk segment.
- Lowers expected portfolio losses by nearly **$160 million**.
- Improves overall portfolio credit quality while affecting only a small portion of total lending volume.
- Supports more conservative and sustainable credit risk management.

---

# Recommendation

The analysis suggests that rejecting applicants with the combined characteristics of:

- very low credit scores,
- low income,
- and high debt-to-income ratios,

can improve overall portfolio quality with only a limited reduction in lending activity.

Although the portfolio default rate improves by only **0.17 percentage points**, the policy reduces expected portfolio losses by **3.73%**, demonstrating that a targeted underwriting strategy can generate meaningful financial benefits without materially shrinking the overall loan portfolio.

Rather than applying broad restrictions across all borrowers, focusing on the highest-risk segment allows the institution to preserve the vast majority of lending activity while substantially reducing expected credit losses.