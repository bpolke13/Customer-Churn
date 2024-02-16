# Customer Churn Analysis
Flatiron School Data Science Project - Phase II

## Overview
* Purpose: To be able to predict whether or not a customer will churn based on given feature values
* Source of data: Sourced data from Kaggle, roughly 500,000 individual customer feature sets 
* Focus areas and consideration:
  * Focused on finding the features that effected churn ratios the most
  
* Data excluded - excluded one line that was mostly NaN values


 
# Presentation and Sources
Presentation: [Link](https://docs.google.com/presentation/d/1op2-2IenyHfKqqI0heit0fu8pDb4qngjclAbbmKx6ME/edit#slide=id.g2b957eebc62_0_180)



# Repository Navigation
Our Github Repository contains 2 Jupyter Notebooks: the NN_Notebook contains the neural network model and the training matrix. The Phase_4_Project notebook contains the data cleaning and the Decision Tree Model. The two csv files contain all the data used to train and test the models.

## Data Analysis & Recommendations

The first step I took was to start bucketing features into segments that would be more useful for business analytics (age, spend, things like that) After that I started to look a thte distributinos of each feature and the ratio of churned clients to non-churned clients at each feature level. Taking some of the more prominent features like Subscription type, calls to support, and amount spent. These features we can see have certain categories that have extremely high churn rates:


![image](https://github.com/bpolke13/Customer-Churn/assets/151547876/fded10c3-e664-4011-a00b-08cfcbffb665)

![image](https://github.com/bpolke13/Customer-Churn/assets/151547876/ddd631b4-2dc3-4f1f-870e-5857e5e1714f)

![image](https://github.com/bpolke13/Customer-Churn/assets/151547876/2f0398c7-f000-41d9-9e9a-eadeb9cb7ca5)


After that I did a train test split and fit the data to a decision tree model. The feature importances it came up with are similar to my EDA analysis.

![image](https://github.com/bpolke13/Customer-Churn/assets/151547876/b1141803-aa8d-4f3f-baf4-ef43fad93b4a)



After that I created a neural network model that performed slightly better than the decision tree model, but both are over 85% accurate which is enough to prove validity.
 

Based on the breakdown we reviewed from the EDA and our models, we can look at the features with higer churn rates and make some changes to improve our business model.

Higher customer support calls lead to higher churn, possible directions:
  1) Retrain customer support staff
  2) Go through recorded calls to see prominent issues

Monthly subscribers are also high churners:
  1) only offer quarterly and annual subscriptions
  2) offer discounts for signing up for longer
  
  Any of these options could lead to better customer retention that would lead to real dollar savings for telecom companies.



