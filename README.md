# Project Traffic Analysis
Personal projects - ML &amp; datascience basics

1. Project Traffic Analysis

Introduction
Every year, the Belgian government releases a full list of all traffic incidents that occurred in Belgium. 
In this notebook, I will construct a model that can help predict the expected number of accidents in a given day. 
I will limit our research to only the accidents that occurred in Flanders and Brussels. This is because certain features, such as traffic density statistics, were only available to me for these regions.

The dataset
The basis of our analysis will consist of an aggregated list of traffic accidents that occurred in Belgium in 2016, 2017 & 2018. 
We will filter out all accidents that did not occur in Flanders or Brussels. We will supplement this dataset with various other date- & weather related information:

Average traffic density per month
Total number of kilometers travelled per month
Average rainfall per month
Temperature per day
Indicators showing if a date falls in a weekend or on a national holiday
See part 3 - Cleaning, for a full list of all features

Models
The used models are seperated in two different chapters:

Descriptive models: the main goal here is to see if there are any interesting correlations between # of accidents per day and other information related to the same calendar date. These cannot be seen as predictive models in themselves however, as they contain information that cannot fully be known in advance, such as the average temperature per day.
* Basic linear regression
* XGBoost
* Linear regression with rolling window
Predictive models: in this part, we will not use any features if we cannot know the value for future dates.
* Time-series forecasting with Meta's Prophet
* Basic linear regression
