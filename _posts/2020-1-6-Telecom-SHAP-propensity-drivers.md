---
layout: post
title: Telecom case study - Using SHAP for explaining propensity drivers!
published: true
---

Business Problem:
We are trying to identify the drivers which will identify customers who are more likely to accept an offer (for up-sell)



[Source Data File](https://www.kaggle.com/skylord/telecom-case-study)

[Kaggle Kernel](https://www.kaggle.com/skylord/using-shap-for-identifying-propensity-drivers)

The notebook is also shared via my repo: 100 days of ML 

[Link to Colab Notebook](https://github.com/skyprince999/100-Days-Of-ML/blob/master/Day%20%233-Telecom_case_study%2C_identifying_propensity_drivers.ipynb)

![Pulling the curtain on black box models](/images/Pulling_apart_curtains-768x510.jpg)


We convert the business problem to a data modeling problem:

A propensity model to capture a large percentage of top decile customers


Steps that we take to create a base model:

- Read the data and run 'pd.profiling'
- Perform some basic EDA
- Since most of the variables have few unique values, convert them to categorical 
- Create dummy variables
- Create a baseline model using (XGBoost, LGBM & Logistic Regression)
- Plot out the feature importance
- Identify interaction using shap values 


Next steps:

- Use intution from model explanation to engineer more variables
- These engineered variables are then used to iteratively create more relevant models
- Hype-tune the new models 


