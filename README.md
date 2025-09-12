This project is about analyzing Facebook ads performance. Data is dummy data created with OpenAI.

# Research problem 
Company X is an education center which sells courses on different topics. It runs Facebook ads to find participants into the courses. The companys marketing team wants to know how well the different ads are performing. 

# Research plan 
The main question is how efficient is the campaign. For that, we calculate the return on ad spend = revenue from course signups divided by the cost of ads. 
We can also measure click-through-rate and compare it to historical average. This shows how well the ad itself is performing. 

# Dataset
The dataset is a CSV file with data from Facebook including: 
Campaign - This is campaign name. 
,Ad Set,Ad,Impressions,Clicks,CTR (%),CPC (USD),Conversions,Spend (USD)

# Business Glossary 
Return on ad spend - revenue from signups divided by the cost of the ad. 

# Data model 
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

