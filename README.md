# Gstore Revenue Management
### Keywords: Customer Segmentation, RFM Analysis, Predictive Analysis, Spark MLlib, 80/20 Rule, Traffic-to Sales Conversion
Data: Gstore Customer Traffic Dataset\
Data source: https://www.kaggle.com/c/ga-customer-revenue-prediction (train.csv)

## Overall Descriptive Analysis (EDA)
Findings:
- 80/20 Rule: Only 1.6% of visitors contributed to the revenue.
- Huge discrepancy between the trend of revenue ($) and number of unique visitors (#) over time during October to December 2016. Might result from the opending of Gstore's temporary pop-up showroom and a store-within-a-store named Google Shop during those two months. So these two events probably largely increased the brand awareness of GStore and brought in lots of visits to it, however, the conversion rate didn’t seem to be ideal and the company didn’t benefit much from those events during that period. 

## User Level: Customer Segmentation Using RFM analysis
- Calculate the RFM (Recency, Frequency, Monetary) of each visitor.
- Divide Recency into 4 tiers, Frequency into 2 tiers and Monetary into 4 tiers.
- Segment the customers based on previous categories.
- Provide corresponding marketing strategy for each segment.

## Transaction Level: Revenue Prediction Model (Random Forest) Using MLlib in Spark 
- Use Random Forest to train the model, and pick out the four most important features that contributed to the transaction revenue, which are city, browser, visit month, and marketing channel.
- Do further descriptive analysis on each of them to give business recommendations based on the traffic to sales conversion rate.
