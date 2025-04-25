 1. Is there a significant difference in median value of houses bounded by the Charles river or not? (T-test for independent samples)

Hypotheses:
- Null (H₀): There is no significant difference in the median value of houses (MEDV) between those bounded by the Charles river (CHAS=1) and those not (CHAS=0).
- Alternative (H₁): There is a significant difference in the median value of houses between the two groups.

Test: Independent samples t-test

Test Statistic:
- The t-test compares the means of MEDV for CHAS=1 vs. CHAS=0.
- From the literature, the correlation between CHAS and MEDV is low (around 0.1), suggesting a minimal effect[4].

Conclusion:
- If the p-value > 0.05, fail to reject H₀: No significant difference in median values.
- If the p-value ≤ 0.05, reject H₀: Significant difference exists.
- In practice, most analyses find the difference is not statistically significant, so we typically fail to reject the null hypothesis[4].

---

2. Is there a difference in Median values of houses (MEDV) for each proportion of owner-occupied units built prior to 1940 (AGE)? (ANOVA)

Hypotheses:
- Null (H₀): The median value of houses (MEDV) does not differ across different AGE groups.
- Alternative (H₁): At least one AGE group has a different median value.

Test: One-way ANOVA (if AGE is grouped, e.g., quartiles)

Test Statistic:
- ANOVA F-statistic tests if means of MEDV differ across AGE groups.
- The variable AGE is the proportion of units built before 1940; it is often divided into bins for ANOVA[3][7].

Conclusion:
- If the p-value ≤ 0.05, reject H₀: There is a significant difference in MEDV between at least two AGE groups.
- If the p-value > 0.05, fail to reject H₀: No significant difference.
- In most studies, older areas (higher AGE) tend to have lower MEDV, and ANOVA often finds significant differences[7].

---

3. Can we conclude that there is no relationship between Nitric oxide concentrations and proportion of non-retail business acres per town? (Pearson Correlation)

Hypotheses:
- Null (H₀): There is no linear relationship between NOX (nitric oxide concentration) and INDUS (proportion of non-retail business acres).
- Alternative (H₁): There is a linear relationship between NOX and INDUS.

Test: Pearson correlation coefficient

Test Statistic:
- Compute Pearson’s r between NOX and INDUS.
- In the Boston dataset, NOX and INDUS are highly positively correlated (r ≈ 0.76), indicating a strong relationship[4].

Conclusion:
- If p-value ≤ 0.05, reject H₀: There is a significant linear relationship.
- If p-value > 0.05, fail to reject H₀.
- The correlation is statistically significant, so we reject the null hypothesis and conclude there is a relationship[4].

---

4. What is the impact of an additional weighted distance to the five Boston employment centres on the median value of owner-occupied homes? (Regression analysis)

Hypotheses:
- Null (H₀): The regression coefficient for DIS (distance to employment centers) is zero (no impact).
- Alternative (H₁): The regression coefficient for DIS is not zero (there is an impact).

Test: Linear regression (MEDV as dependent variable, DIS as predictor)

Test Statistic:
- The regression coefficient for DIS indicates the change in MEDV for each unit increase in DIS.
- Studies show the coefficient for DIS is positive, meaning greater distance from employment centers is associated with higher MEDV, but the effect is moderate[4][10].

Conclusion:
- If p-value for DIS coefficient ≤ 0.05, reject H₀: Distance significantly impacts MEDV.
- If p-value > 0.05, fail to reject H₀.
- Most analyses find a statistically significant positive effect, so we reject the null hypothesis and conclude that distance to employment centers has a significant impact on house prices[4][10].

---

Summary Table

| Question                                                                 | Test Used                | Main Finding/Conclusion                                                                 |
|--------------------------------------------------------------------------|-------------------------|----------------------------------------------------------------------------------------|
| Charles river boundary and MEDV difference                               | Independent t-test      | No significant difference in most analyses                                              |
| MEDV differences by AGE (pre-1940 units)                                 | ANOVA                   | Significant differences exist; older areas often have lower MEDV                        |
| NOX vs. INDUS (non-retail business) relationship                         | Pearson correlation     | Strong positive correlation; significant relationship exists                            |
| Impact of distance to employment centers (DIS) on MEDV                   | Linear regression       | Significant positive effect; further distance can increase MEDV                         |

