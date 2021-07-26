# Bank Customer Churn Prediction
For a business in a stipulated period of time, customers can come under 3 major categories
 
1. Newly Acquired Customers
2. Existing Customers
3. Churned Customers

Customer churn/attrition is a tendency of customers to abandon a brand and stop being a paying client of a particular business.

Churned Customers means a direct loss of Marketing Acquisition Cost and possible revenue which could be capitalized post sale. Hence, predicting possible customers who can churn beforehand can help us save this loss. In order to retain them, they need to identify the customers as well as the reason of churning so that they can provide the customers with personalized offers and products. The aim of our project is to solve this problem for banking domain, by identifying which customers are at risk of churning and what are the reasons for churning with the help of supervised learning classification alogorithms.

# Data Set
In this project we are using a source of 10,000 bank records to predict the likelihood of a customer churn. You can  [click here ](https://www.kaggle.com/barelydedicated/bank-customer-churn-modeling) to get access to the raw data.

# Data Cleaning:
We removed unnecessary variables such as row number, customer names and IDs to make the dataframe more readable. Now, we are left with the below Columns:
* Age
* Balance
* CreditScore
* Estimated Salary
* Exited
* Geography
* Gender
* HasCrCard
* IsActiveMember
* NumberOfProducts
* Tenure

# EDA
As part of analyzing the data, we plotted different predictors against the target variable, i.e the number of people and tried to see if any patterns emerge. Two such plots are worth looking into.

---

### Customer Churn by Geography and Gender
![image](https://user-images.githubusercontent.com/44424472/126912085-ba789af5-2a6d-4d9f-8468-4e55dd9807ec.png)

The smallest number of customers are from Germany, and they are also the most likely to leave the bank. Almost one in three German customers in our sample left the bank.
In percentage, female customers are more likely to leave the bank at 25%, compared to 16% of males.

---

### Customer Count by Exit Status
![Churn by Exit Status](https://user-images.githubusercontent.com/44424472/126026664-1e0ccd6e-db2b-4db6-bb89-4b94ab833b31.PNG)

The majority class, "Stays" (0), has around 80% data points and the minority class, "Exits" (1), has around 20% datapoints.
So the baseline model could be to predict that 20% of the customers will churn. Given 20% is a small number, we need to ensure that the chosen model does predict with great accuracy this 20% as it is of interest to the bank to identify and keep this bunch as opposed to accurately predicting the customers that are retained. So instead of looking only at overall model accuracy, we will should also focus on recall.

---

### Distribution Analysis:
![Density Plots](https://user-images.githubusercontent.com/44424472/126027391-d4f81e7c-0a2b-499e-9d7d-b6a8ca4cf5e1.PNG)

From density plots we can see that customer with more products and older customer are more often leaving the bank. We can also observe that customer having only 2 products has very less churn rate.

![Density Plots - Balance](https://user-images.githubusercontent.com/44424472/126043629-2ef9ec8d-a945-41c9-8294-c38fee26ad6c.PNG)

Customers having balance between 85,000 to 1,50,000 tend to churn more.
