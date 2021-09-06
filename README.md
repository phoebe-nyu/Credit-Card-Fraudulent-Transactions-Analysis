# Credit-Card-Fraudulent-Transactions-Analysis

## Introduction
One of the greatest concerns of many business owners is how to protect their company from fraudulent activity. Nowadays, fraud detection plays a more important role in business world, especially for banks. 

## Dataset
Our dataset comes from Capital One Data Science Challenge.It's a very large dataset, with 800,000 transaction records and 29 columns. 
https://github.com/CapitalOneRecruiting/DS

## Methods 
1.  **EDA**: I first implemented EDA(histogram,boxplot,etc) and correlation analysis for transactions, in order to bring out actionable insights/hypothesis. 
From EDA part, I noticed fraud are more likely to happen in small transactions rather than large transactions. Hence, banks should better focus on protecting small transactions from customers.

2.  **Data Wrangling**: After analyzing dataset, I found some transactions looked like duplicated transactions. Usually, there are two kinds, one is a reversed transaction, where a purchase is followed by a reversal. Another is multi-swipe, where a vendor accidentally charges a customer's card multiple times within a short time span.
  For multi-swipe transaction, I defined that similar transactions(with same account number and transaction amount) in 10 minutes are multi-swipe, looping for overal dataset, and got 13304 records of multi-swipe transactions, with 1,917,460.02 dollars total amount. 
  
3.   **Model**: Considering it's a very imbalanced dataset with many categorical variables, I used one hot encoding and SMOTE firts. By applying Logistic Regression, I established my baseline model. I used Random Forest and Xgboost to improve model performance. Also, extract important features by implementing feature importance. 
