# Wellness

## About this project
Main task of the project is to analyze smart device usage data in order to gain insight into how consumers use non-Bellabeat smart
devices and apply these insights into one Bellabeat product. Discovered insights will help guide marketing strategy for the company. 

**Task:** explore user’s data to uncover trends and patterns in daily activities and identify key wellness indicators of healthy lifestyle.

**Questions:**
 - What are some trends in smart device usage?
 - What specific metrics indicate a more active lifestyle?
 - How could these trends impact Bellabeat marketing strategy?

## About data
Dataset “FitBit Fitness Tracker Data” was generated by respondents to a distributed survey via Amazon Mechanical Turk between 04.12.2016-05.12.2016 and  kindly provided through [Mobius](https://www.kaggle.com/datasets/arashnic/fitbit?select=Fitabase+Data+4.12.16-5.12.16). Dataset consists of 18 csv files of 33 users who consented to provide personal tracker data that includes output for physical activity, heart rate, sleep monitoring, and  steps. Some tables are organized in long format, some organized in wide format. Upon closer examination we discovered that not all tables of the dataset have the same number of unique user Ids. For example, 'sleep_day' table has 24, 'daily_activity' - 33, and 'heart_rate_seconds' has only 8 unique users. These findings will limit some aspects of further analysis. To answer the above mentioned questions we decided to study the following metrics recorded daily: calories, total steps, total distance, different intensity minutes, time asleep, time in bed, heart rate.

**Tables**: daily_activity.csv, daily_calories.csv, heart_rate_seconds.csv, sleep_day.csv


## Cleaning process 
Considering that the number of observations in some tables reach over 1 millions rows, we decided to use BigQuery Studio to perform our data manipulations. We created a new dataset named ‘fitbit’ and uploaded all csv files while assigning new names following standards of naming conventions.

First, ensuring that the dataset is clean we checked Field and Type of data in the SCHEMA of selected tables. 

