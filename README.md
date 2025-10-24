# This project is an example of using PPDAC model for data analysis.

If you have any questions about the project, please reach out by email: ranivirve@gmail.com 

# Problem 
Company X is an education center which sells courses on different topics. It runs Facebook ads to find participants into the courses. The companys marketing team wants to know how well the different ads are performing. 

# Plan 
The main question is how efficient is the campaign. For that, we calculate the return on investment = revenue from course signups divided by the cost of ads. 
We can also measure click-through-rate and compare it to historical average. This shows how well the ad itself is performing.
For data, a dummy dataset was created with OpenAI. Therefore, no data privacy laws need to be taken into consideration while using the solution.

# Data

### Business Glossary 
(Only one example is brought, an actual glossary would have all terms described)

Return on investment (ROI) - revenue from signups divided by the cost of the ad. 

### Data glossary
(Only few examples are brought, an actual data description would have all columns described.)

| Source System | Source Column | DWH Column | Column Format | Description
| ----------- | ------------- | --------------|---------------|------------ |
| Facebook API  | Campaign     | CampaignName | String   | Name of the marketing campaign.
| CSV from marketing team| Course Name     | CourseName | String   | Name of the course.

### Data model

This dataset includes three tables with info on ads performance, courses and number of paid customers from ads:
1) ads_dummy_dataset has information coming from Facebook about the ads performance.
2) ads_paidcustomers table has information on how many customers ended up paying for the course.
3) ads_courses has information on the price of the course.


<img width="666" height="654" alt="image" src="https://github.com/user-attachments/assets/a5e3bc47-e6eb-4837-ac32-280cfb588f1e" />



### Data lineage 
We take data from Facebook as a CSV file and upload it to Power BI. 
<img width="540" height="135" alt="image" src="https://github.com/user-attachments/assets/51ce2f7a-a9b1-4846-8b52-7ee3516c5b10" />

### Data tables description
(Only one example is brought, an actual description would include all tables)

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


# Analysis
We created an ad comparison table which shows converison rates and return on investment.

Based on this dummy dataset, the Ad 7 performed the best and Ad 4 performed the worst.

<img width="858" height="476" alt="image" src="https://github.com/user-attachments/assets/8d779435-9afd-4f54-867b-d793dec2f47c" />


# Conclusion 
Based on this dummy dataset, the best performing ads were: Ad7 and Ad9.

It would be beneficial to additionally gather qualitative feedback on the ads.










