# The Detail

Food Panda Data Set from Pakistan
Link : https://www.kaggle.com/datasets/nabihazahid/foodpanda-analysis-dataset-2025

The Detail

This dataset contains customer-level transactional and behavioral data from a food delivery platform.Each record represents one customer, summarized from their historical order activity.

This Data Captures
- Purchasing behavior (price, quantity, order frequency)
- Customer engagement over time (recency, tenure)
- Loyalty and value indicators
- Basic contextual attributes (payment method, city)

The target variable, churn_flag, indicates whether a customer has become inactive. This dataset is used to analyze customer behavior, identify churn drivers, and build predictive churn models.

# Executive Summary

The analysis identifies customer churn driven primarily by declining engagement rather than pricing. Exploratory Data Analysis shows that Recency and Frequency are the strongest indicators of churn, while price per order has minimal impact.The outcome is a data-driven early warning system, integrating RFM analysis with predictive modeling, enabling prioritized retention actions and more sustainable churn reduction.


# The Purpose

Key Objectives

- Analyze behavioral patterns of churned Foodpanda customers to uncover the true drivers of disengagement beyond price
- Identify and validate key churn drivers through exploratory data analysis to understand who the core customers are and why they leave
- Develop a churn prediction model (≥75% accuracy) to enable early identification of high-risk customers

What This Project Delivers

- Clear identification of behavioral churn signals (e.g., recency and frequency decline)
- A predictive early warning system to flag customers before they churn
- Customer segmentation combining churn risk and customer value (CLV)
- Actionable insights that guide who to retain, when to act, and how to personalize engagement

Value Proposition 

These insights enable the business to act earlier, target smarter, and grow revenue sustainably through data-driven customer decisions.


# Data Dictionary

<img width="529" height="530" alt="image" src="https://github.com/user-attachments/assets/2b07be73-beff-4fbb-8c3e-91d7c7783b34" />

Link https://docs.google.com/spreadsheets/d/1srnmpO-yM5rV1-iT0rWhTP16h0Qvr0ruV2nE_0aN3jc/edit?usp=sharing

# The questions 

<img width="719" height="270" alt="image" src="https://github.com/user-attachments/assets/21e0ccb9-8d29-40e4-9e35-79a93662b0ab" />

# Exploratory Data Analysis
<img width="833" height="434" alt="image" src="https://github.com/user-attachments/assets/4e605035-1046-4f5b-bc12-848ca795fc09" />

(The above visualization is selected for this topic analysis)

# Key Findings

- **High Churn Risk**: Churn rate is as high as 46%, indicating that nearly half of customers leave the platform, directly impacting revenue and business stability.
- **Loss of High-Value Customers**: Churned customers have a higher AOV than active customers (805 vs 797), showing that the business is losing high-value (VIP) customers, not low-quality ones.
- **Weakening Key Revenue Markets**: High-income cities such as Multan and Lahore experience churn rates above 47%, signaling revenue risk in strategic geographic markets.
- **Behavioral Decline Before Churn**: Churned customers exhibit lower purchase frequency, higher days since last order, and longer tenure, confirming that churn is preceded by a gradual decline in engagement rather than sudden exit.

# Hypothesis

H₀ (Null Hypothesis):
Customer churn rate has no significant relationship with the business’s total revenue.

H₁ (Alternative Hypothesis):
Customer churn rate has a significant relationship with the business’s total revenue,
such that an increase in churn leads to a decrease in total revenue.

# Cleaning Data

1. Data Quality & Integrity
Assessed completeness, logical consistency, and duplicates
Identified critical issues affecting churn and revenue analysis
2. Temporal & Behavioral Validation
Corrected date inconsistencies and invalid order sequences
Revalidated Recency, Frequency, and engagement metrics
3. Feature & Target Standardization
Standardized churn into binary format for modeling
Corrected misclassified categories and loyalty indicators
4. Revenue & Value Construction
Created revenue and monetary features
Enabled CLV and value-based analysis
5. Model Readiness
Encoded categorical and demographic variables
Final validation to ensure EDA- and ML-ready data

# Analysis

**Box Plot Distribution**

<img width="480" height="283" alt="image" src="https://github.com/user-attachments/assets/0004ce0c-7f25-47be-bebb-4264460933a1" />

- Customer heterogeneity and skewed revenue distributions make average-based analysis insufficient for decision-making.
- Behavioral signals (recency, frequency, engagement) emerge as early indicators of churn, outperforming price and rating variables.
- The analysis must shift from descriptive patterns to individual churn risk estimation.
- Integrating churn risk with Customer Lifetime Value (CLV) enables prioritization of value-destructive churn rather than churn volume alone.

Next Step 
- RFM analysis is the necessary next step to convert exploratory behavioral insights into structured, business-interpretable customer segments.


**Box Plot Churn and Active**

<img width="406" height="293" alt="image" src="https://github.com/user-attachments/assets/992c1293-0007-47a1-b9ba-3eada72dd913" />

The price distribution between Active and Inactive customers is highly similar.
- The median price of both groups is nearly the same.
- The interquartile range (IQR) and maximum values largely overlap across the two groups.

Insight
- Order price is not a key driver of churn.
- Customers who churn do not exhibit a clearly lower spend per order compared to active customers.

**Correlation Matrix**

<img width="359" height="322" alt="image" src="https://github.com/user-attachments/assets/d8979baf-de4b-4c1f-92fd-b407de3031dd" />

Correlation Heatmap (Numeric Features)
- Most numeric variables show correlations close to zero.
- Quantity and price per item exhibit a strong negative correlation (≈ -0.66).
-Price and price per item show a moderate positive correlation (≈ 0.58).
- Churn-related variables (order_frequency, days_since_last_order, loyalty_points) show no clear linear relationship with revenue-related variables.

Insight
- Purchasing behavior is complex and non-linear.
- Customers who order larger quantities tend to choose lower-priced items per unit.
- Spend per order is not a primary driver of churn.
- Churn is better explained by temporal and frequency-based behaviors (recency, frequency, engagement) rather than revenue alone.

**Hypothesis Testing: Active vs. Inactive Customers**

<img width="438" height="293" alt="image" src="https://github.com/user-attachments/assets/95d23cec-6708-4240-a527-ea083d9cc99d" />

Test
An independent two-sample, two-tailed t-test was performed to compare the mean sales value (price) between Active and Inactive customers.

H₀ (Null Hypothesis):
The average sales of Active and Inactive customers are equal.
H₁ (Alternative Hypothesis):
The average sales of Active and Inactive customers are different.

- Significance Level (α): 0.05

**Results**
- T-statistic: -0.7969
- P-value: 0.4255

## Conclusion

Since p-value > 0.05, **we fail to reject H₀.**

There is no statistically significant difference in average sales between Active and Inactive customers.
This suggests that churn is not driven by order value, but is more likely explained by behavioral factors such as recency, frequency, and engagement.


# Consolidate Insight

Shift from price-based tactics to behavior-driven retention.
Focus on recency, frequency, and engagement, not discounts.

**Churn Drivers**

1. Price per unit  is not the main cause of churn. customers who churn do not necessarily spend less per order than active customers.Therefore Price discounting is not a sustainable churn solution.

2. Churn is a behavioral problem, not a revenue problem. Customers churn primarily due to declining engagement and purchase activity, not low spend.

**Key Metrics: Recency & Frequency**

1. Recency & Frequency are critical signals
   Longer time since last purchase and lower purchase frequency are stronger churn indicators than total spend or order value.

**Customer Segmentation for Action**

1.About to Sleep / At-Risk

= High churn risk → requires immediate reactivation actions.

2. Potential / Need Attention

= Still valuable → high return on retention investment.

**Strategic Approach**

Use an RFM system as an early-warning mechanism
to prioritize:

Retention campaigns

Win-back campaigns

Avoid mass discounting as a default strategy.

# RFM Model Analysis 

<img width="990" height="353" alt="image" src="https://github.com/user-attachments/assets/400c09d5-68df-4e11-b8bd-7dd393002245" />
Key Finding

| Area | Data Observation | Business Insight | Decision / Action |
|------|------------------|------------------|-------------------|
| Customer Base | Most customers fall into Champion, Loyal, and Potential segments | The customer base remains valuable; churn is not widespread | Prioritize retaining existing customers |
| Churn Risk | About to Sleep and At-Risk segments show high recency and low frequency | Churn is driven by purchase inactivity, not order value | Focus on retention and win-back campaigns |
| Value Driver | No significant difference in monetary value per order | Price is not a primary churn driver | Reduce reliance on discount-led strategies |
| Behavior Signal | Recency and frequency clearly separate churn groups | Time-based behavior predicts churn effectively | Use RFM as an early-warning system |
| Resource Allocation | Potential / Need Attention customers still have high value | This segment offers the highest ROI for intervention | Prioritize campaigns for this group first |


---

# Answering Our Questions: From Behavior to Business Impact


## 1. How does customer purchasing behavior evolve before churn?

Customer churn is preceded by **progressive disengagement**, not an abrupt revenue drop.  
Customers show **lower purchase frequency** and **longer time since last order (high recency)** well before becoming inactive, while spend per order remains relatively stable.

**Key Insight:**  
Churn develops over time through declining engagement, making it **predictable in advance**.


## 2. Which factors drive churn: behavior vs. price?
Statistical validation (two-sample t-test, distribution overlap, correlation analysis) confirms that **order value and price-related metrics do not differ significantly** between Active and Inactive customers.  
In contrast, **recency and frequency strongly differentiate churn states**.

**Driver Hierarchy:**
- **Primary:** Time-based and engagement behaviors  
- **Secondary / Weak:** Monetary value and price

**Key Insight:**  
Churn is a **behavioral phenomenon**, not a pricing problem.



## 3. Which customer features consistently separate churned customers?
The most robust churn indicators across segmentation and heatmaps are:
- **Recency** (time since last purchase)
- **Frequency** (purchase regularity)
- **Loyalty engagement signals**

Monetary metrics show high variance and strong overlap between churned and active customers, limiting their diagnostic value.

**Key Insight:**  
Reliable churn differentiation requires **behavioral and temporal features**, not average spend.


## 4. How can churn be predicted early and reliably?
An **RFM-based early warning system** identifies customers moving into **About to Sleep** and **At-Risk** segments before revenue loss occurs.  
This behavior-first approach reduces missed high-risk customers and supports more effective predictive modeling.

**Key Insight:**  
Early churn prediction depends on **when and how customers disengage**, not how much they spend.



## 5. How should churn insights be applied to business decisions?
Churn analytics should be operationalized through **value-aware prioritization**:
- Protect **Champions and Loyal** customers via retention programs  
- Prioritize **Potential / Need Attention** segments for highest ROI  
- Apply targeted **Win-back** strategies to At-Risk customers  
- **Avoid mass discounting**, which treats symptoms rather than causes  

This enables efficient budget allocation and sustainable churn reduction.

---

## Executive Takeaway
**Churn is a behavioral, time-dependent problem—not a pricing problem.**  
Sustainable retention requires **early detection through recency and frequency signals**, combined with **value-based prioritization**, rather than revenue-driven or discount-led tactics.


