***Understanding Lender Behavior on Kiva’s Crowdfunding Platform***

Project Overview

This project aims to analyze the key characteristics and behaviors of lenders on Kiva's crowdfunding platform. By understanding these factors, we can gain insights

into what drives lending decisions, which can improve various aspects of the platform, from loan recommendations to user engagement.# Kiva-Data-Research

Research Question

What are the key characteristics and behaviors of lenders on Kiva's crowdfunding platform, and how do these factors influence their lending decisions?

Objectives
1) Understand lender attributes and behaviors on Kiva

2) Improve loan recommendations and user engagement

3) Identify key lender characteristics and behaviors for personalized recommendations

Data Overview
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
