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
