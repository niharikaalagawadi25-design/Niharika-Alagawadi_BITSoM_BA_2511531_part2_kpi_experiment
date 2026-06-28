
# Task 6: Hypothesis Test Notes

## Objective

The objective of this experiment is to determine whether the Treatment group performs differently from the Control group in converting users into paid customers.

---

## 1. Null Hypothesis (H₀)

There is **no statistically significant difference** in the paid conversion rate between the Control group and the Treatment group.

**H₀:** Paid Conversion Rate (Control) = Paid Conversion Rate (Treatment)

---

## 2. Alternative Hypothesis (H₁)

There **is a statistically significant difference** in the paid conversion rate between the Control group and the Treatment group.

**H₁:** Paid Conversion Rate (Control) ≠ Paid Conversion Rate (Treatment)

---

## 3. Type of Test

**Two-tailed test**

### Reason

The purpose of the experiment is to determine whether the Treatment causes any significant change in the paid conversion rate compared to the Control group. A two-tailed test checks for both an increase and a decrease in performance.

---

## 4. Significance Level

**α = 0.05 (5%)**

A significance level of 0.05 means that a p-value less than 0.05 will be considered statistically significant.

---

## 5. Metric Being Tested

**Paid Conversion Rate**

**Formula:**

Paid Conversion Rate = Number of users converted to paid / Total number of users

---

## 6. Reason for Choosing This Metric

Paid Conversion Rate is the primary Key Performance Indicator (KPI) for this experiment because it directly measures the percentage of users who become paying customers.

An increase in the paid conversion rate indicates that the Treatment is more effective than the Control version and has a direct impact on business revenue.

---

## 7. Interpretation Logic

* If **p-value < 0.05**

  * Reject the Null Hypothesis (H₀).
  * Conclude that there is a statistically significant difference between the Control and Treatment groups.
  * If the Treatment has a higher conversion rate, recommend implementing the Treatment.

* If **p-value ≥ 0.05**

  * Fail to reject the Null Hypothesis (H₀).
  * Conclude that there is insufficient evidence to say the Treatment performs differently from the Control.
  * Recommend keeping the current version or collecting more data before making a decision.

---

## Business Decision

The outcome of this hypothesis test will help determine whether the new Treatment should replace the existing Control version.

* If the Treatment significantly improves the paid conversion rate, it should be deployed to all users.
* If there is no statistically significant improvement, the current Control version should be retained and further experimentation may be conducted.
----------------------------------------------------------------------------------------------------------------



## Task 7: Perform Hypothesis or A/B Test Analysis

# Hypothesis Test Notes

## Objective

The objective of this A/B test was to determine whether the **Treatment** group resulted in a statistically significant improvement in the **Paid Conversion Rate** compared to the **Control** group.

Paid Conversion Rate was selected as the primary evaluation metric because it directly measures the percentage of users who successfully converted into paying customers, making it the most important indicator of the experiment's success.

# Primary Metric

**Paid Conversion Rate**

Formula:
Paid Conversion Rate = (Number of Converted Users ÷ Total Users) × 100

# Hypotheses

## Null Hypothesis (H₀)
There is **no statistically significant difference** in the paid conversion rate between the Control and Treatment groups.

Null hypo:Treatment = Control

This assumes that any observed difference in conversion rates occurred due to random variation.
---

## Alternative Hypothesis (H₁)
The Treatment group has a **higher paid conversion rate** than the Control group.

H1: Treatment > Control

This suggests that the new treatment positively influences user conversion.
---

# Test Method

An **Independent Two-Sample t-Test (Assuming Unequal Variances)** was performed using **Microsoft Excel's Data Analysis ToolPak**.

The converted column contained binary values (1 = Converted, 0 = Not Converted). The test compared the average conversion outcomes between the Control and Treatment groups to determine whether the observed difference was statistically significant.

---

# Test Inputs

| Item                   | Value                                 |
| ---------------------- | ------------------------------------- |
| Experiment Groups      | Control vs Treatment                  |
| Primary Metric         | Paid Conversion Rate                  |
| Statistical Test       | Two-Sample t-Test (Unequal Variances) |
| Significance Level (α) | 0.05                                  |
| Confidence Level       | 95%                                   |

---

# Test Output

| Metric                    |       Result |
| ------------------------- | -----------: |
| Control Conversion Rate   |    **3.19%** |
| Treatment Conversion Rate |    **7.04%** |
| p-value                   | **0.001026** |

---

# Decision Rule

* If **p-value < 0.05**, reject the Null Hypothesis.
* If **p-value ≥ 0.05**, fail to reject the Null Hypothesis.

Since:

**0.001026 < 0.05**

the Null Hypothesis is **rejected**.

---

# Business Interpretation

The hypothesis test demonstrates that the Treatment group achieved a **statistically significant improvement** in Paid Conversion Rate compared to the Control group.

The Control group recorded a Paid Conversion Rate of **3.19%**, while the Treatment group achieved **7.04%**, representing more than a twofold increase in user conversions. The calculated **p-value of 0.001026** indicates that the probability of observing such an improvement purely by random chance is approximately **0.10%**, which is far below the chosen significance level of 5%.

This provides strong statistical evidence that the Treatment had a positive effect on user purchasing behaviour. The improved conversion rate suggests that the changes introduced in the Treatment group—such as modifications to the user experience, landing page, pricing presentation, or onboarding flow—were more effective at encouraging users to become paying customers.

From a business perspective, implementing the Treatment has the potential to increase revenue by converting a larger proportion of users into paying customers. However, before deploying the Treatment to all users, it is advisable to continue monitoring secondary performance indicators such as refund requests, support ticket volume, customer satisfaction, and long-term user retention to ensure that the higher conversion rate does not negatively impact overall customer experience.

---

# Conclusion

Based on the results of the hypothesis test, the Treatment group significantly outperformed the Control group in terms of Paid Conversion Rate.

Because the **p-value (0.001026)** is substantially lower than the significance level of **0.05**, there is sufficient statistical evidence to conclude that the Treatment improves user conversion. Therefore, the experiment supports recommending the Treatment for wider implementation, while continuing to monitor key business metrics after deployment to validate sustained performance.
