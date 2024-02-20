## Table of Content
[Introduction](#introduction)

[Dataset](#dataset)
* [Data Dictionary](#data-dictionary)

[Hypothesis](#hypothesis)

[Analytical Questions](#analytical-questions)

[Data Preparation](#data-preparation)

[Modeling & Evaluation of Models](#modeling--evaluation-of-models)

[Result](#result)

[Recommendation](#recommendation)

[Links](#links)

# Predicting Customer Churn (A Study for Vodafone)
# Introduction
To gain new customers in an organisation often incurs more cost compared to selling to current customers. As such, it will be important to predict the churn rates of customers to assist in identifying potential customers who might want to leave. Companies that can identify customers who are at high risk of leaving will focus on their efforts and incentives of retaining those specific customers. It will also help to create appropriate marketing strategies to retain customers.

This projects aims to to gain insights in the data by identifying factors of customer churn and developing a model that can predict a customer churn in Vodafone.
The project's results will enable Vodafone to handle customer attrition with greater expertise and initiative.

# Dataset
The datasets used for this project were sourced from 3 different sources, i.e. github repository, OneDrive file, and an SQL database

<h2>Data Dictionary</h2>

The following describes the columns present in the data.

Gender -- Whether the customer is a male or a female

SeniorCitizen -- Whether a customer is a senior citizen or not

Partner -- Whether the customer has a partner or not (Yes, No)

Dependents -- Whether the customer has dependents or not (Yes, No)

Tenure -- Number of months the customer has stayed with the company

Phone Service -- Whether the customer has a phone service or not (Yes, No)

MultipleLines -- Whether the customer has multiple lines or not

InternetService -- Customer's internet service provider (DSL, Fiber Optic, No)

OnlineSecurity -- Whether the customer has online security or not (Yes, No, No Internet)

OnlineBackup -- Whether the customer has online backup or not (Yes, No, No Internet)

DeviceProtection -- Whether the customer has device protection or not (Yes, No, No internet service)

TechSupport -- Whether the customer has tech support or not (Yes, No, No internet)

StreamingTV -- Whether the customer has streaming TV or not (Yes, No, No internet service)

StreamingMovies -- Whether the customer has streaming movies or not (Yes, No, No Internet service)

Contract -- The contract term of the customer (Month-to-Month, One year, Two year)

PaperlessBilling -- Whether the customer has paperless billing or not (Yes, No)

Payment Method -- The customer's payment method (Electronic check, mailed check, Bank transfer(automatic), Credit card(automatic))

MonthlyCharges -- The amount charged to the customer monthly

TotalCharges -- The total amount charged to the customer

Churn -- Whether the customer churned or not (Yes or No)


# Hypothesis
Null Hypothesis:A  Customer's contract term do not affect churning rate.

Alternative Hypothesis: Customers with shorter contract term affects churning rate.

# Analytical Questions
1. What is the total churning rate of the customers?
 
2. What is the total amount of money senior and non senior citizens are charged? 

3. what is the churning rate of senior citizens?

4. What is the most used payment method for customers?

5. Does contract term of a customer affect churning rate?

6. Is there a difference in churn rate amongst males and females?

7. Do customers with dependants have a shorter contract term?

# Data Preparation
The collected dataset needed to be put right because it contained null values and incorrect data types in some of the columns. Simple Imputer was used to impute the null values, and data types for columns with incorrect data types were set right.

To guarantee that the same procedures were applied whenever new datasets were made available, the appropriate modifications were added to a pipeline. OneHot Encoder and Label Encoder were used to convert all of the dataset's category columns to numerical values so that the machine-learning model could learn effectively.

# Modeling & Evaluation of Models
In order to build a robust machine-learning model, five classification models were trained. These models includes DecisionTree,RandomForest, LogisticRegression, GradientBoosting and SupportVectorMachine classifiers.

To improve performance of the model, there was a feature selection and hyperparameter tuning for the best performing model.

The performance of the model was assessed using the f1-score, presicision and accuracy metric as well as the AUC-ROC curve.

# Result 
LogisticRegression classifier was the best performing model and that was used in the prediction of the churn rate/ number of the test dataset.

Out of a total of 2000 customers, the model was able to predict that 436 customers churned while 1564 cutomers did not churn.

# Recommendation
From the insights above, vodafone should engage these 436 customers who churned to increase their revenue for the upcoming years. 

# Links
Find below links to visualization of analysis using Tableau and also an article published on medium

https://medium.com/@baakwadegraftmiah/unveiling-patterns-predicticting-customer-churn-b36c1f040479

