
# Recommendation Memo

## Task 1: Business Problem Summary

The company conducted an A/B experiment to evaluate a new onboarding campaign designed to improve user activation and early engagement.

The purpose of the A/B experiment is to determine whether the new onboarding and activation campaign should replace the existing onboarding experience for all users. The decision impacts leadership, product, marketing, customer success teams, and users. The primary success metric is the conversion rate to paid subscriptions, supported by engagement and revenue metrics. Leadership must also monitor guardrail metrics such as support tickets and refund requests to ensure the new experience does not negatively affect customer satisfaction. A recommendation should only be made if the treatment group demonstrates meaningful improvements in conversion and engagement without creating unacceptable business risks.

The final recommendation will be based on KPI analysis, statistical testing, guardrail evaluation, and segment-level performance before deciding whether to launch the new onboarding experience to all users.
--------------------------------------------------------------------------------------------------------------------


# Task 9: Write Recommendation Memo

1. Executive Summary

The objective of this A/B experiment was to determine whether the new onboarding campaign (Treatment) should replace the existing onboarding experience (Control). The analysis focused on improving the North Star Metric—User Activation Rate, while ensuring that increases in conversions did not negatively affect customer experience or business performance.

The experiment produced strong evidence that the Treatment outperformed the Control. The Paid Conversion Rate increased from 3.19% in the Control group to 7.04% in the Treatment group, representing more than a twofold improvement. Statistical testing confirmed that this improvement was significant (p-value = 0.001026 < 0.05), indicating that the observed increase is highly unlikely to have occurred by chance.

However, business decisions should not rely solely on conversion improvements. Guardrail metrics revealed a slight increase in refund requests and support tickets, suggesting that while more users were converting, some experienced confusion or unmet expectations after onboarding. At the same time, engagement scores improved and the average time required to convert remained stable, indicating that the new onboarding experience successfully encouraged user interaction without slowing the conversion journey.

Overall, the Treatment delivers substantially better business outcomes than the Control and provides a strong basis for rollout, provided that customer experience metrics continue to be monitored after launch.


2. North Star Metric

North Star Metric: User Activation Rate

User Activation Rate was selected because the primary objective of the campaign is to move new users successfully through onboarding and into active product usage.

Improving activation creates a positive chain of business outcomes:

Better onboarding experience → Higher user engagement → More trial starts → Higher paid conversions → Increased subscription revenue

Supporting KPIs such as Trial Start Rate, Paid Conversion Rate, Engagement Score, and Average Revenue per User measure the downstream effects of successful activation. However, optimizing activation alone without monitoring customer satisfaction could lead to users converting quickly but becoming dissatisfied later, making guardrail metrics equally important.


3. KPI Tree Explanation

The KPI Tree demonstrates how User Activation Rate is influenced by three major business drivers:
a. Onboarding Completion

Users who successfully complete onboarding are significantly more likely to explore product features and continue through the customer journey.

Primary drivers:
Landing Page Visit Rate
Onboarding Completion Rate

A smooth onboarding process reduces user drop-offs and increases the likelihood of conversion.

b. User Engagement

Engaged users spend more time interacting with the platform, increasing familiarity and perceived value before making a purchase decision.

Primary drivers:
Trial Start Rate
Average Engagement Score

Higher engagement strengthens user confidence and naturally improves conversion probability.

c. Subscription Conversion

The final objective is transforming activated users into paying customers.

Primary drivers:
Paid Conversion Rate
Average Revenue per User

Improved onboarding and engagement ultimately translate into stronger business revenue.

To ensure growth remains sustainable, the KPI Tree also includes Guardrail Metrics:
Refund Rate
Support Ticket Rate
Average Days to Convert
Revenue Quality

These metrics ensure that higher conversions are not achieved at the expense of customer satisfaction or long-term profitability.

4. Experiment Result Summary

The experiment clearly demonstrates that the new onboarding campaign improves business performance.

Key observations include:
- Paid Conversion Rate increased from 3.19% (Control) to 7.04% (Treatment).
- More users successfully progressed through the onboarding journey and became paying customers.
- Average Engagement Score improved under the Treatment, indicating that users interacted more actively with the product.
- Average Days to Convert remained relatively stable, meaning users converted faster or at a similar pace despite the onboarding changes.
- Average Revenue per User also improved because the Treatment generated more paying customers.

The relationship between these metrics suggests that the new onboarding experience successfully reduced friction in the customer journey. Rather than simply convincing more users to purchase, it encouraged greater engagement, which ultimately translated into higher conversions.

5. Hypothesis Test Interpretation

An Independent Two-Sample t-Test (Unequal Variances) was performed to compare the Paid Conversion Rate between the Control and Treatment groups.

Results:
Control Conversion Rate: 3.19%
Treatment Conversion Rate: 7.04%
p-value = 0.001026
Significance Level (α) = 0.05

Since: 0.001026 < 0.05

the Null Hypothesis was rejected.

This provides strong statistical evidence that the Treatment genuinely improves Paid Conversion Rate rather than the improvement being caused by random variation.

From a business perspective, leadership can be confident that the new onboarding campaign has a measurable positive impact on customer acquisition and subscription growth.

6. Guardrail Analysis

While the Treatment increased conversions, it also introduced several customer experience considerations.

I. Refund Rate:
Refund requests increased slightly in the Treatment group.

This suggests that some users converted successfully but later felt the product did not fully meet their expectations. Possible causes include:
- unclear pricing communication,
- unrealistic expectations created during onboarding,
- users purchasing before fully understanding the product.

Although the increase is relatively small, continued monitoring is recommended because rising refund rates reduce net revenue.

II. Support Ticket Rate:
Support tickets also increased slightly after introducing the new onboarding experience.

This may indicate that while onboarding successfully encouraged users to convert, certain steps were confusing or required additional assistance.

Potential causes include:
- insufficient onboarding guidance,
- unclear feature explanations,
- users encountering issues immediately after activation.

Improving tutorials, FAQs, and in-app guidance could reduce support costs without sacrificing conversion improvements.

III. Engagement Score:
Engagement scores improved under the Treatment.

This is an encouraging signal because higher engagement usually reflects increased product exploration and stronger customer interest before conversion.

Higher engagement also improves the likelihood of long-term customer retention.

IV. Average Days to Convert:
Days to Convert remained relatively unchanged.

This indicates that the new onboarding experience successfully increased conversions without extending the customer's decision-making process.

Overall, the guardrail metrics reveal manageable operational risks rather than major business concerns.

7. Segment-Level Insight

Segment-level analysis showed that the Treatment generally outperformed the Control across multiple customer groups, including Region, Device Type, and Traffic Source.

Although performance improvements were broadly consistent, some segments responded more positively than others.

For example:

- Certain traffic sources demonstrated stronger conversion improvements, suggesting that users arriving through those channels aligned better with the new onboarding experience.
- Mobile and desktop users both benefited from the Treatment, indicating that the onboarding flow performs consistently across devices.
- Regional performance remained balanced, suggesting that the campaign is suitable for a broad customer base rather than a single geographic market.

These findings indicate that the Treatment is scalable across multiple customer segments while still allowing future optimization for underperforming groups.

8. Final Recommendation
Recommendation: Launch

Based on the experiment results, the new onboarding campaign should be launched.

This recommendation is supported by several factors:

Paid Conversion Rate more than doubled.
Statistical testing confirmed the improvement is significant (p-value = 0.001026).
Engagement increased.
Conversion speed remained stable.
Revenue potential improved through higher customer acquisition.

Although refund requests and support tickets increased slightly, these risks are relatively small compared with the significant gains in conversion performance and can be managed through ongoing monitoring and incremental onboarding improvements.

The expected increase in subscription revenue outweighs the operational risks identified during the experiment.

9. Risks and Limitations

Several limitations should be considered before a full rollout.

The experiment primarily measures short-term behaviour and does not evaluate long-term customer retention.
Refund and support metrics should continue to be monitored after deployment.
High-value revenue outliers may influence average revenue calculations.
Some customer segments may require additional optimization despite overall positive results.
External factors such as seasonal behaviour or marketing campaigns were not included in this analysis.

These limitations suggest that post-launch monitoring remains essential.

10. Next Steps

To maximize the value of the new onboarding campaign, the company should:
- Deploy the Treatment to all users through a phased rollout.
- Continuously monitor refund rates and support ticket trends during the first few weeks after launch.
- Analyze customer feedback to identify friction points within the onboarding flow.
- Improve onboarding documentation, tutorials, and in-app guidance to reduce customer confusion.
- Track long-term retention, customer lifetime value (CLV), and churn to confirm that higher conversions translate into sustainable business growth.
- Conduct follow-up A/B experiments to further optimize onboarding steps for lower-performing customer segments.