# Error Analysis

## Overview

The churn model was evaluated using both false positives and false negatives. False positives represent customers predicted to churn who ultimately stayed, while false negatives represent customers predicted to stay but actually churned.

From a business perspective, false negatives are generally more costly because they represent missed retention opportunities. However, excessive false positives can also increase campaign costs and reduce marketing efficiency.

---

# False Positive Analysis

## Customer CUST00044

The model predicted churn, but the customer remained active. The customer had moderate engagement through Google Search acquisition and may have exhibited temporary inactivity that resembled churn behavior.

## Customer CUST00109

The model predicted churn, but the customer stayed. The customer's recent activity likely declined temporarily, causing the model to classify them as high risk despite continued loyalty.

## Customer CUST00335

This customer was predicted as a churn risk but remained active. The prediction may have been influenced by lower purchase frequency or reduced engagement signals.

## Customer CUST00437

The model identified this customer as likely to churn, but the customer continued purchasing. Marketplace-acquired customers may have irregular purchase cycles that resemble churn patterns.

## Customer CUST00491

The customer was predicted to churn but remained active. Organic acquisition customers often return after periods of inactivity, which can create false alarms.

### Business Risk of False Positives

False positives increase campaign spending because retention incentives may be offered to customers who would have remained active without intervention. However, the business impact is generally limited compared with losing valuable customers.

---

# False Negative Analysis

## Customer CUST00184

The model predicted retention, but the customer churned. As a Platinum-tier customer, the model may have relied too heavily on historical loyalty indicators.

## Customer CUST00247

The customer churned despite being classified as low risk. Behavioral changes may have occurred after the snapshot date that were not captured in the training features.

## Customer CUST00414

The model missed this churn event. Marketplace customers may display stable historical behavior before suddenly disengaging.

## Customer CUST00438

This Platinum-tier customer churned unexpectedly. Strong loyalty signals likely outweighed subtle warning signs during prediction.

## Customer CUST00531

The customer churned even though the model predicted retention. The available engagement signals may not have fully reflected declining customer satisfaction.

### Business Risk of False Negatives

False negatives are the most costly prediction errors. These customers receive no retention intervention and may be permanently lost, resulting in lost revenue, reduced customer lifetime value, and higher future acquisition costs.

---

# Key Findings

1. High-tier customers can still churn despite strong historical loyalty signals.
2. Temporary inactivity can cause customers to be incorrectly classified as churn risks.
3. Marketplace and referral-acquired customers exhibit less predictable behavior patterns.
4. Loyalty status alone should not be relied upon as a predictor of future retention.
5. Additional behavioral features and customer satisfaction indicators may further improve model performance.

# Recommendations

1. Prioritize reducing false negatives through threshold optimization.
2. Incorporate additional engagement and support-related signals.
3. Monitor performance separately across loyalty tiers.
4. Periodically retrain the model to capture changing customer behavior.
5. Use model predictions as decision support rather than the sole basis for retention campaigns.
