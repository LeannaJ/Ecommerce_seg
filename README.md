# Exploring the effectiveness of customer segmentation 
Using real-world e-commerce data, I intend to propose effective customer segmentation for enhancing business strategies. 
I could gain insights into their behavior patterns and purchasing trends.

## Description
Apply various customer segmentation techniques such as RFM, Cohort, and Clustering analysis to derive meaningful insights from the given data, and propose innovative business solutions based on these results.

## Approaches
### Customer Segmentation Techniques
- RFM Analysis: Use Recency, Frequency, and Monetary metrics to categorize customers into segments based on their recent activity, purchase frequency, and spending amount.
- Cohort Analysis: Group customers into cohorts based on shared characteristics and analyze their behavior over time.
- Cluster Analysis: Apply clustering algorithms (such as K-means) to segment customers based on multiple variables.

### Define Variables
- **Recency**: Days since last transaction
- **Frequency**: Number of transactions in 2019
- **Monetary**: Total transaction amount in 2019

### Insight Derivation
- _The RFM segments are defined using quantile analysis._
- _It is necessary to use less sensitive scaler(RobustScaler) because of outliers for F & M variables._
- _Set the weights of RFM with K-Means and calculate the final RFM score._

**Five of customer grades: standard, silver, gold, black, and platinum**
> `Black & Platinum` customers account for approximately 38% of the total number of customers, and contribute about 78% of the total revenue. Thus, it is essential to focus on `Black & Platinum` customers segment.
>> examine detailed RFM segments for this purpose

### Business Solution Proposal
1. `Black & Platinum` customer group is primarily distributed in the upper right side.
- BUT, there are also some customers with relatively lower RFM values.
- Therefore, a more detailed segmentation of the customer group is necessary for finer analysis.
2. Detailed segmentation
- `VIP`: All R,F,M >=4
- `Churn`: Low R (R<=3)
- `Potential`: Low F (F<=3)
- `Loyal`: Low M (M<=3)
