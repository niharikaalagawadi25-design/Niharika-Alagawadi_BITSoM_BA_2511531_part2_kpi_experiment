
# Part 2: KPI Framework, Business Experiment Analysis & Decision Recommendation

## Task 1: Business Problem Statement

### Business Context

The company is a subscription-based digital product provider that aims to improve user onboarding and early engagement. To achieve this, a new onboarding and activation campaign has been introduced. Users were randomly assigned to one of two groups:

* **Control Group:** Existing onboarding experience
* **Treatment Group:** New onboarding experience

The objective of this A/B experiment is to determine whether the new onboarding experience performs better than the existing one.

### 1. Decision to Be Made

The primary business decision is whether the new onboarding campaign should be launched to all users or whether the company should continue using the existing onboarding process.

### 2. Who the Decision Impacts

This decision affects several stakeholders, including:

The decision affects several stakeholders, including:

* Senior Leadership, who are responsible for strategic business decisions.
* Product Management, who manage the onboarding experience.
* Marketing Team, who focus on user acquisition and activation.
* Customer Success Team, who support user engagement and retention.
* Existing and future users, whose onboarding experience will be affected.

A successful rollout could improve customer acquisition, engagement, and long-term revenue, while a poor rollout could negatively affect user experience and business performance.

### 3. Metric That Should Improve

The primary success metric for this experiment is the **User Activation Rate**, measured by the percentage of users who successfully complete onboarding and begin actively using the product.

Supporting metrics include:

* Trial Start Rate
* Paid Conversion Rate
* Average Revenue per User
* Engagement Score

### 4. Risks That Must Be Monitored

The company should not evaluate success based only on increased activation. Important guardrail metrics must also be monitored to ensure the new onboarding experience does not negatively impact users.

These include:

* Increased support tickets due to user confusion.
* Higher refund requests resulting from customer dissatisfaction.
* Reduced customer engagement after onboarding.
* Lower short-term revenue despite improved conversion.
* Average Days to Convert
* Segment-level performance

### 5. Evidence Required Before Making a Recommendation

Before recommending a full rollout, the experiment should demonstrate that the treatment group performs better than the control group on the primary success metric while maintaining acceptable guardrail metrics.

* The Treatment group performs better than the Control group on the primary KPI.
* The improvement is statistically significant.
* Guardrail metrics remain stable or improve.
* No important customer segment experiences worse performance.
* The experiment results are based on sufficient and reliable data.
* No significant increase in support tickets or refund requests.
* Overall business benefit that justifies implementing the new onboarding experience for all users.

Only after meeting these conditions should the company recommend launching the new onboarding campaign to all users.

------------------------------------------------------------------------------------------------------------------------------------------

# Task 2: Define the North Star Metric

## Selected North Star Metric

**User Activation Rate**

### Why this is the Main Success Metric

The primary goal of the new onboarding campaign is to help new users successfully complete the onboarding process and begin actively using the product. Therefore, **User Activation Rate** is the most appropriate North Star Metric because it directly measures whether the new onboarding experience is achieving its intended objective.

Users who become activated are more likely to start a free trial, convert to a paid subscription, remain engaged with the product, and generate long-term revenue. Since activation is the first major milestone in the customer journey, improving this metric has a direct impact on the overall success of the business.

### Why Other Metrics Are Supporting Metrics

Although several other metrics are important, they are considered supporting metrics because they measure outcomes that occur after user activation or monitor the quality of the onboarding experience.

* **Trial Start Rate** indicates how many activated users begin a trial, but it depends on successful activation.
* **Paid Conversion Rate** measures how many users become paying customers after activation.
* **Average Revenue per User (ARPU)** reflects the financial outcome of successful activation.
* **Engagement Score** measures how actively users interact with the product after onboarding.
* **Refund Rate** and **Support Ticket Rate** are guardrail metrics that help identify potential issues but do not directly measure onboarding success.

These metrics provide valuable supporting information but do not directly represent the primary objective of the experiment.

### How the North Star Metric Connects to Business Growth

The conversion rate to paid subscriptions is directly linked to the company's long-term growth because every successful conversion increases the number of paying customers.

Higher conversion rates can lead to:

- Increased subscription revenue.
- Improved customer acquisition efficiency.
- Higher customer lifetime value.
- Better return on marketing and product investments.
- Sustainable business growth through a larger paying customer base.

Improving this metric indicates that the onboarding campaign is effectively moving users from initial interest to becoming paying customers.


### Risks of Optimizing This Metric Blindly

Focusing only on User Activation Rate may lead to unintended consequences. For example:

* Users may complete onboarding without understanding the product.
* Low-quality activations may increase while long-term retention decreases.
* Support ticket volume may rise.
* Revenue quality may decline if users activate but do not remain paying customers.
* Encouraging users to subscribe through misleading offers or aggressive promotions that increase future refund requests.
* Increasing short-term conversions without improving long-term customer retention or profitability.

For this reason, User Activation Rate should always be evaluated together with guardrail metrics such as Refund Rate, Support Ticket Rate, Revenue per User, Engagement Score, and Days to Convert before making a final business recommendation.
----------------------------------------------------------------------------------------------------


# Task 4 – Clean and Prepare Experiment Data

## Data Quality Checks

### 1. Missing Values
The dataset contains missing values in the following columns:

| Column           | Missing Values |Handling                                                                      |
| ---------------- | -------------: | ------------------------
| device_type      |             18 | Filled with "Unknown"                                         |
| traffic_source   |             24 | Filled with the "Unknown"                                         |
| engagement_score |             14 | Filled with median value.                                                 |
| days_to_convert  |           1336 | Left as NULL because users who did not convert do not have a conversiontime. |

### 2. Group Counts
For Raw data:
* Control: 693 users
* Treatment: 715 users

For clean data:
* Control: 690 users
* Treatment: 710 users

The experiment groups are reasonably balanced. No action required.

### 3. Duplicate User IDs

Eight duplicate user IDs were identified.

Action:

* Remove exact duplicate records while keeping one unique record per user.
* If duplicate IDs contain conflicting information, review them before analysis.

### 4. Invalid Binary Values

The following binary columns were checked:

* visited_landing_page
* started_trial
* completed_onboarding
* converted_to_paid
* refund_requested

All values are valid (0 or 1). No cleaning required.

### 5. Revenue Outliers

72 revenue outliers were identified using the IQR method.

Action:

* Flag outliers for review.
* that outliers were detected using the IQR method and retained because they may represent genuine high-value customers.


### 6. Segment Distribution Across Groups

| Plan Type | Control | Treatment |
| --------- | ------: | --------: |
| Free      |     361 |       368 |
| Basic     |     223 |       235 |
| Premium   |     109 |       112 |

The distribution of customer segments across experiment groups is balanced. No action required.

## Summary

The dataset required:

* Imputing missing values in `device_type`, `traffic_source`, and `engagement_score`.
* Retaining missing values in `days_to_convert`.
* Removing or resolving 8 duplicate user IDs.
* Reviewing (but not automatically removing) 72 revenue outliers.

All other checks passed without requiring modifications.
--------------------------------------------------------------------------------------------------------------------



# Task 8: Guardrail Metrics Evaluation

## Purpose

Although the Treatment group demonstrated a statistically significant improvement in **Paid Conversion Rate**, business decisions should not rely solely on conversion performance. Several **guardrail metrics** were evaluated to ensure that the increase in conversions did not negatively impact customer satisfaction, operational efficiency, or revenue quality.

---

## 1. Refund Rate

### Observation

The Treatment group recorded a slightly higher refund rate than the Control group.

### Business Risk

An increase in refund requests may indicate that some users converted because of the new onboarding experience but later decided that the product did not meet their expectations. Higher refund rates reduce net revenue and may negatively affect customer trust.

### Recommendation

Continue monitoring refund behaviour after rollout. Analyse refund reasons to identify whether they are caused by pricing expectations, onboarding clarity, or product experience.

---

## 2. Support Ticket Rate

### Observation

The Treatment group generated a slightly higher support ticket rate than the Control group.

### Business Risk

A higher support ticket rate suggests that users may require additional assistance during onboarding or shortly after conversion. This increases customer support workload and operational costs.

### Recommendation

Review the most common support issues raised by Treatment users. Improving onboarding instructions, FAQs, and in-app guidance could reduce support requests while maintaining higher conversion rates.

---

## 3. Average Days to Convert

### Observation

The average number of days required for users to convert remained relatively consistent between the Control and Treatment groups.

### Business Risk

No significant business risk was identified for this metric. Users continued to convert within a similar timeframe, indicating that the new onboarding process did not slow the customer journey.

### Recommendation

Continue tracking this metric after deployment to ensure future updates do not increase the time required for users to convert.

---

## 4. Average Engagement Score

### Observation

The Treatment group achieved a slightly higher average engagement score than the Control group.

### Business Risk

No immediate risk was identified. Increased engagement indicates that users interacted more actively with the product before converting, which is generally associated with stronger customer adoption and long-term retention.

### Recommendation

Monitor engagement trends alongside retention metrics to confirm that increased engagement translates into sustained customer value.

---

# Overall Guardrail Assessment

The hypothesis test confirmed that the Treatment significantly improved the Paid Conversion Rate (**p-value = 0.001026**). However, evaluating the guardrail metrics revealed that the Treatment also produced a modest increase in refund requests and support ticket volume.

These increases do not outweigh the improvement in conversion, but they highlight areas that should be monitored after rollout. The stable conversion time and improved engagement score indicate that the new onboarding experience remains effective without introducing major usability concerns.

---

# Final Assessment

The Treatment is recommended for rollout because it delivers a statistically significant increase in Paid Conversion Rate while maintaining acceptable performance across the evaluated guardrail metrics.

To minimise potential risks, the company should:

* Monitor refund requests after deployment.
* Track support ticket trends to identify onboarding issues.
* Continue measuring engagement and conversion time.
* Conduct periodic reviews of customer feedback and retention.

This balanced evaluation ensures that the recommendation considers both business growth and customer experience rather than relying solely on higher conversion rates.
