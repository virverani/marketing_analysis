This project is about analyzing Facebook ads performance. Data is dummy data created with OpenAI.

# Research problem 
Company X is an education center which sells courses on different topics. It runs Facebook ads to find participants into the courses. The companys marketing team wants to know how well the different ads are performing. 

# Research plan 
The main question is how efficient is the campaign. For that, we calculate the return on ad spend = revenue from course signups divided by the cost of ads. 
We can also measure click-through-rate and compare it to historical average. This shows how well the ad itself is performing. 

# Business Glossary 
Return on ad spend - revenue from signups divided by the cost of the ad. 

# Data model and data glossary
This dataset includes one table with ads info. 

# Data lineage 
We take data from Facebook as a CSV file and upload it to Power BI. 
<img width="540" height="135" alt="image" src="https://github.com/user-attachments/assets/51ce2f7a-a9b1-4846-8b52-7ee3516c5b10" />


# Data table description 
| Source System | Source Column | DWH Column | Column Format | Description
| ----------- | ------------- | --------------|---------------|------------ |
| Facebook API  | Campaign     | CampaignName | String   | Name of the marketing campaign.

# Creation of dummy dataset 
Based on this data table OpenAI created a dummy dataset to be analyzed.

| Column Name | Column Format | Description                                                                      |
| ----------- | ------------- | -------------------------------------------------------------------------------- |
| Campaign    | String        | Name of the marketing campaign.                                                  |
| Ad Set      | String        | Name of the ad set within the campaign.                                          |
| Ad          | String        | Name or identifier of the individual ad.                                         |
| Impressions | Integer       | Number of times the ad was displayed to users.                                   |
| Clicks      | Integer       | Number of times users clicked on the ad.                                         |
| CTR (%)     | Float         | Click-through rate, calculated as (Clicks ÷ Impressions) × 100.                  |
| CPC (USD)   | Float         | Cost per click in USD, calculated as Spend ÷ Clicks.                             |
| Conversions | Integer       | Number of desired actions completed (e.g., course signups) attributed to the ad. |
| Spend (USD) | Float         | Total amount spent on the ad in USD.                                             |


# Power BI semantic model 
Power BI semantic model has 3 source tables: 
1) ads_dummy_dataset which has information coming from Facebook about the ads performance.
2) ads_paidcustomers table which has information on how many customers ended up paying for the course.
3) ads_courses has information on the price of the course.

Semantic model in Power BI: 
<img width="666" height="654" alt="image" src="https://github.com/user-attachments/assets/a5e3bc47-e6eb-4837-ac32-280cfb588f1e" />

# Analysis results
We created an ad comparison table which shows.....

Based on this dummy dataset, the Ad 7 perfomormed the best and Ad 4 performed the worst.

<img width="858" height="476" alt="image" src="https://github.com/user-attachments/assets/8d779435-9afd-4f54-867b-d793dec2f47c" />


# Conclusion 
Based on this dummy dataset, the best performing ads were: 

The difference between ad performance was.....

This report can be used to add more data and ads comparison to monitor the performance over time. You can download the Power BI file for that from this link: 












