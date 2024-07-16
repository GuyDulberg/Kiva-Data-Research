![image](https://github.com/user-attachments/assets/6fe2b7bb-aee1-4e79-9093-fda94d95fe47)***Understanding Lender Behavior on Kiva’s Crowdfunding Platform***

Project Overview

This project aims to analyze the key characteristics and behaviors of lenders on Kiva's crowdfunding platform. By understanding these factors, we can gain insights

into what drives lending decisions, which can improve various aspects of the platform, from loan recommendations to user engagement.# Kiva-Data-Research

Research Question

What are the key characteristics and behaviors of lenders on Kiva's crowdfunding platform, and how do these factors influence their lending decisions?

**Objectives**

1) Understand lender attributes and behaviors on Kiva

2) Improve loan recommendations and user engagement

3) Identify key lender characteristics and behaviors for personalized recommendations

**Data Overview:***

The dataset comprises several tables with information about lenders and micro-loans on Kiva’s crowdfunding platform:

Bigml and loans: Details about loan applicants, unique loan identifiers, loan amounts, and other attributes.

lenders: Contains unique usernames, occupations, and other personal details of registered lenders.

loans_lenders: Connects unique loan identifiers to the unique usernames of lenders.

We constructed a new table named TreeTableLoaners with engineered variables:

Lender_Username: Unique lender identifier.

Gender_Loan_Preference: Gender most frequently lent to by the lender.

Average_Age_Range_of_Borrower: Average age of borrowers to whom the lender lent.

Average_Loan_Amount_Range: Average loan amount lent by the lender.

Loan_Sector: Most mentioned loan sector in the loans the lender took part in.

Borrower_Country: Country with the most borrowers the lender lent to.

Borrower_Continent: Continent with the most borrowers the lender lent to.

Lender_Cause_to_Lend: Reason for registering.

Lender_Occupation: Lender's occupation.

**Methods and Results**
Data Preparation and Feature Engineering

We imported and cleaned the data from the Bigml, loans, lenders, and loans_lenders tables, creating the TreeTableLoaners table with engineered features. One-hot

encoding was applied to handle categorical data, resulting in the One-Hot Encode - TreeTableLoaners – Category table.

**Clustering and Classification**

We used k-means clustering to categorize lenders based on their characteristics, determining 12 clusters as the optimal number using the elbow method.

To understand the defining characteristics of each cluster, we calculated the mean of each feature’s value for each cluster group and set thresholds based on the

mean plus two standard deviations. Descriptive strings summarizing cluster profiles were generated for values exceeding these thresholds.

**Classification Model**

We developed a random forest classification model to predict lender groups based on their characteristics, achieving an accuracy of 0.809. The random forest 

classifier identified Borrower_Continent, Average_Age_Range, and Gender_Loan_Preference as significant predictors of lender group membership.

**Key Results**

Geographic and demographic factors are key in influencing lending decisions.

The importance of categories in the model is illustrated in the graph below.

**Conclusion**

Our analysis highlights the complexity of lender behaviors on Kiva. By clustering lenders and analyzing feature importance, we identified key characteristics 

influencing lending decisions, such as regional preferences, demographic factors, and sectoral focus. Understanding these characteristics allows Kiva to improve 

loan recommendations, aligning them with lender preferences and enhancing the platform’s efficiency and impact.

**Data and Code**

Link to our data folder

Link to our code repository on GitHub

Authors
Oren Raz,
Shaked Shabat,
Ilay Damary,
Guy Dulberg
