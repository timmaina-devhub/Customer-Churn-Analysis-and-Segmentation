# Customer Churn Analysis and Segmentation Project

## Project Overview

This project analyzes customer behavior in an e-commerce setting to understand the drivers of churn and identify actionable opportunities to improve retention. The work combines data cleaning, exploratory analysis, feature engineering, machine learning, and customer segmentation to deliver both predictive and strategic insights.

The primary objective is to answer three key questions:

* Why are customers churning?
* Which customers are at risk?
* What actions can improve retention and revenue?

---

## Dataset and Preparation

The dataset consisted of transaction-level customer data, including order activity, monetary value, and timestamps. Initial exploration revealed several data quality challenges:

* Inconsistencies between order dates and signup dates
* Lack of repeat customer structure in earlier iterations
* Ambiguity in refund and transaction status

To address this:

* Date inconsistencies were corrected to maintain logical sequencing
* Customer-level features were engineered using RFM (Recency, Frequency, Monetary) principles
* Churn labels were defined based on inactivity (recency threshold)
* Refund behavior was standardized using transaction amounts

These steps ensured the dataset was analytically consistent and suitable for both modeling and segmentation.

---

## Methodology

### Feature Engineering

Customer-level features were created to capture behavioral patterns:

* Recency: Time since last purchase
* Frequency: Number of purchases
* Monetary: Total spend
* Average Order Value

These features formed the foundation for both predictive modeling and clustering.

---

### Churn Prediction

Multiple classification models were trained and evaluated, including:

* Logistic Regression
* Random Forest
* Other baseline classifiers

Logistic Regression was selected as the final model due to its balance of performance and interpretability:

* Precision: 72.53%
* Recall: 93.63%
* F1 Score: 81.74%
* Accuracy: 75.35%

The model demonstrated strong ability to identify churned customers, particularly through high recall.

---

### Customer Segmentation

K-Means clustering was applied to the RFM dataset to group customers into distinct behavioral segments. The optimal number of clusters (5) was determined using silhouette analysis.

The resulting segments represent different customer profiles, including:

* High-value loyal customers
* At-risk customers with declining engagement
* New or low-engagement customers
* Low-value occasional buyers
* Lost or inactive customers

This segmentation provides a structured view of the customer base beyond simple churn classification.

---

## Key Findings

* Churn rate is high, with more customers leaving than remaining active, indicating a significant retention issue.
* Customer inactivity (recency) is a major driver of churn, making it a critical early warning signal.
* Purchase frequency is the strongest predictor of retention; more engaged customers are significantly less likely to churn.
* Refund behavior is closely associated with churn, suggesting dissatisfaction with product or service experience.
* High spending does not guarantee loyalty, meaning valuable customers are still at risk of leaving.
* Customer distribution is skewed toward at-risk and low-engagement segments, while high-value loyal customers form a smaller proportion of the base.

---

## Business Recommendations

* Focus on re-engaging at-risk customers through targeted campaigns and personalized offers.
* Investigate and address the root causes of refunds to improve customer satisfaction and reduce churn.
* Retain high-value customers with loyalty programs and tailored incentives.
* Increase purchase frequency through promotions, reminders, and engagement strategies.
* Improve onboarding and early engagement for new customers to encourage repeat purchases.

---

## Dashboard and Communication

An interactive dashboard was developed to present:

* Key performance indicators (churn rate, revenue, customer counts)
* Behavioral trends over time
* Customer segmentation insights

Insights and recommendations are integrated into the dashboard to support quick decision-making by stakeholders while maintaining a clean and user-friendly interface.

---

## Challenges and Lessons Learned

* Simulating real-world customer behavior highlighted the importance of preserving data integrity. Artificial manipulation of identifiers and timestamps introduced inconsistencies that required reevaluation.
* Defining churn in the absence of explicit labels required careful consideration and validation.
* Initial models showed unrealistically high performance due to data leakage, reinforcing the need for proper feature selection and validation practices.
* Translating clustering results into meaningful business segments required both analytical and domain understanding.

This project emphasized the importance of balancing technical modeling with practical business interpretation.

---

## Conclusion

The analysis shows that customer churn is primarily driven by low engagement and inactivity, with refund behavior acting as a strong signal of dissatisfaction. By focusing on increasing customer engagement, improving experience, and targeting high-risk segments, the business can significantly improve retention and overall performance.

This project demonstrates the full lifecycle of a data analysis workflow, from raw data challenges to actionable business insights.
