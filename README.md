# Starbucks-Capstone-Project

## Overview and Motivation

In this capstone project, I worked with datasets from Starbucks that contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Once every few days, Starbucks sends out an offer to users of the mobile app. An offer can be merely an advertisement for a drink or an actual offer such as a discount or BOGO (buy one get one free). The task was to combine transaction, demographic and offer data to determine which demographic groups respond best to offers overall. This project derived insights by merging the following 3 datasets:

1. Rewards program users (17000 users x 5 fields)
2. Offers sent during 30-day test period (10 offers x 6 fields)
3. Event log (306648 events x 4 fields)

## Problem Statement

I’ve used the CRISP-DM process to understand the datasets and derive insights to make recommendations to the Starbucks team. Through this capstone project, I wanted to understand the following:

1. How does offer response depend on gender, age and income? 
2. What type of demographic is least affected by offers?
3. What are the top 2 offers for each customer segment?
4. If we're given demographic features about a customer, how can we determine if they'll respond to a BOGO or a discount offer?

## Analysis Summary

1. Impact of Gender, Age and Income

- Females have a higher completion ratio than males. 
- The offer completion % is also increasing as the income level increase
- We can’t conclude over here that the increase in income results in increase in completion % because offers received by the higher income levels is much lesser than that of the lower income levels
- This might be due to the fact that there are fewer customers in the higher income brackets. Starbucks needs to ensure that the higher level income brackets receive more offers per customer than they do currently
- Similarly, with respect to age and gender, females and males between ages 48–68 have received the most number of offers and their offer completion rate is also one of the highest
- We can also see that offer completion ratios for customers between 98–108 years is the highest, and I would caution again to ignore this stat because of the less data we have at our disposal for this age segment

2. Demographic Least Affected by Offers

- Customers with higher income (>$84,000) are mainly concentrated in the medium and low impact category
- Customers between 17 and 30 years of age are also mainly concentrated in the medium and low impact category

3. Top 2 Offers for each customer segment

Please refer to the Jupyter notebook for the detailed analysis

## Conclusion

Overall, this was a great challenging capstone project to test my knowledge from the last 5 months on the course. If I look back at where I started, I wouldn’t ever imagine to be at this place 5 months down the line.

One of the interesting and difficult aspects of this project was it was open-ended and up to me as to how I analyzed and published my recommendation. It was a little daunting when I started but as I got into the problem, it was easy for me to connect the dots and arrive at the results. I was able to answer the questions I had in the beginning. It also was very relatable because in the real world, problems are open-ended and it’s up to the data scientist to figure out how to derive the insights and showcase it to the audience.

## Repository Contents

1. Data Folder

   a. portfolio.json
      * Rewards program users (17000 users x 5 fields)
      * gender: (categorical) M, F, O, or null
      * age: (numeric) missing value encoded as 118
      * id: (string/hash)
      * became_member_on: (date) format YYYYMMDD
      * income: (numeric)
   
   b. profile.json
      * Offers sent during 30-day test period (10 offers x 6 fields)
      * reward: (numeric) money awarded for the amount spent
      * channels: (list) web, email, mobile, social
      * difficulty: (numeric) money required to be spent to receive reward
      * duration: (numeric) time for offer to be open, in days
      * offer_type: (string) bogo, discount, informational
      * id: (string/hash)
   
   c. [transcript.json](https://www.kaggle.com/blacktile/starbucks-app-customer-reward-program-data) Could not upload it here due to size.
      * Event log (306648 events x 4 fields)
      * person: (string/hash)
      * event: (string) offer received, offer viewed, transaction, offer completed
      * value: (dictionary) different values depending on event type
      * offer id: (string/hash) not associated with any "transaction"
      * amount: (numeric) money spent in "transaction"
      * reward: (numeric) money gained from "offer completed"
      * time: (numeric) hours after start of test
      
 2. Starbucks_Capstone_notebook.ipynb: Jupyter Notebook with the Analysis

## Blog Post

I've explained my approach and analysis through a [blog](https://nihalshah1996.medium.com/starbucks-capstone-project-b78d7752d1e4) on Medium

## Libraries

1. pandas
2. numpy
3. math
4. json
5. matplotlib
6. seaborn
7. sklearn

## Authors

[Nihal Shah](https://github.com/NIHALDSM10)


## Acknowledgement

[Kaggle](https://www.kaggle.com/blacktile/starbucks-app-customer-reward-program-data)
[Udacity](https://www.udacity.com/)
[Starbucks](https://www.starbucks.com/)
