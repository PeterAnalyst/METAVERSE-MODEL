# METAVERSE-MODEL(PREDICTIVE ANALYSIS)
---
![](METAVERSE.jpg)
---
## Introduction
---
***This project is about using Excel to create a predictive model to identify transactions with a high risk score. Also to describe the steps one would take, including data preparation, model creation, and validation. Another thing discussed is the functions or add-ins  one could use***



## Problem Statement
1. What Model is best fit to carry-out this prediction and Why?
2. Describe the steps taken including data preparation and model creation.
3. What is the validation of the model?


### 1. What Model is best fit to carry-out this prediction and Why?
   
 The First step is deciding what machine learning model in excel to apply. I decided to use use  because  it is used to describe the relationships between a set of independent variables and the dependent variable. Since the intention is to analyze relationships between other independent variables (Other columns) with one dependent variable( i.e.. the Risk Score), _**Multiple Linear Regression**_ is what i will be using to Predict transactions with _high-risk scores_. [Read More on Why Linear Regression here](https://statisticsbyjim.com/regression/when-use-regression-analysis/)

### 2. Describe the steps taken including data preparation and model creation.

These are the steps taken when building this model

Steps Taken 
 
**Step 1. (DATA CLEANING)**

i. Data inspection and Cleaning: It is important in making sure there are no empty or missing values.
ii. Formatting Inconsistences: It's import that the formating for each colomns are consistent and has the correct data type
iii. Removed Duplicates

**Step 2. (Relationship Creation/Check)**
One of the first things I did was to check for possible relationship between quantitative column(in this case hour_of_day, amount, ip_prefix, login_frequency, session_duration) by using the CORREL Formula and also carried out regression analysis but wasn't comfortable with the R-Suared value as it was considerably low.

**Step 3. (Create Extra Columns)** 

Then I created a dummy variable(ie. creating new columns and using conditional statements whose results are in the form 0 if false and 1 if true) with the qualitative columns to see how its related or affects the Risk Score. For More understanding of dummy variable CLICK [Here](https://www.youtube.com/watch?v=BEapC8Sv8cA) 

**Step 4. (TEST, RETEST and TEST AGAIN 😒)**

This is the most tasking. I tried creating a regression Model using both these dummy columns and the real columns and constantly removed each columns whose p-value is beyond 0.05 or gives a number error (i.e. _**#NUM!**_) 
**Note:** I did not entirely remove the columns based on just the p-value or _**#NUM!**_ error. I started by first taking the ones with the lowest co-efficient values and kept retesting until the p-Values where below 0.05 and R-squared and Adjusted R Square were at least 0.90. [Click read to Understand p-values](https://www.statology.org/linear-regression-p-value/) or [watch this video](https://www.youtube.com/watch?v=CL9MsExcKfU&list=PL-p9JpwN5NNGnXoGDMeF_M6LFUHsjGi0w)

### 3. What is the validation of the model?

To validate this type of model accuracy is of Importance. So some of the statistical formulars i used was  Mean Absolute Percentage Error (MAPE) as it helps me to be sure the error i would get from the model will be minimal and I did get 13% means my Model is 87% Accurate😊

## Conclusion

It is still possible to improve this model as there are possible better approach to predicting model of higher accuracy, But i very much believe this one(model) stands head and shoulder with any other predicted model

