
# Project Dashboard

![Financial Loan Summary](https://github.com/aarzoo-collab/Financial-Loan-/assets/173943221/91185b3c-8d85-4146-a3d1-22d34305a273)


![Financial Loan Overview](https://github.com/aarzoo-collab/Financial-Loan-/assets/173943221/9dcaec06-39d3-4f52-8350-8eff00f6562c)


Financial Loan
Problem Statement: Predicting Loan Outcomes
Background: A financial institution processes loan applications from various customers. These applications can result in either “good” loans (Fully Paid,Current) or “bad” loans (Charge-offs). The institution wants to improve its loan approval process by predicting the likelihood of loan outcomes.
Objective: Develop a predictive model that can accurately classify loan applications as either “good” or “bad” based on relevant features.
Data: The dataset includes historical loan applications with the following features:
Loan amount
Purpose (e.g., car, credit card, educational etc)
Grade (e.g., A,B,C,D,E,F)
Interest rate
Term (36 months or 60 months)
Verification status(Not Verified,Source Verified,Verified)
Home ownership(Mortgage,Rent,Own)
Employment length(in years)






Summary: KPI 
Formulas:
Total Loan Applications: 39K
Total Loan Applications = Count(financial_loan[id])

MTD LOAN APPLICATIONS :4K
MTD Loan Applications = CALCULATE(TOTALMTD([Total Loan Applications],'Date Table'[Date]))

MOM LOAN APPLICATIONS:6.9%
MOM LOAN Apploications = ([MTD Loan Applications] - [PMTD Loan Applications])/[PMTD Loan Applications]

Total Funded Amount: $436 million
Total Funded Amount = Sum(financial_loan[loan_amount])

MTD Funded Amount :54million
MTD Funded Amount = CALCULATE(TOTALMTD([Total Funded Amount],'Date Table'[Date]))

Mom Funded Amount:13%
MOM Funded Amount = ([MTD Funded Amount] - [PMTD Funded Amount])/[PMTD Funded Amount]

Total Amount Received: $473 million
Total Amount Recieved = SUM(financial_loan[total_payment])
MTD Amount Received:58 million
MTD Amount Recieved = CALCULATE(TOTALMTD([Total Amount Recieved],'Date Table'[Date]))

MOM Funded Amount: 15.8%
MOM Amount Recieved = ([MTD Amount Recieved] - [PMTD Amount Recieved])/[PMTD Amount Recieved]


Average Interest Rate: 12.0%
Average Interest Rate = Average(financial_loan[int_rate])

MTD Interest Rate :12%
MTD Average Interest Rate = CALCULATE(TOTALMTD([Average Interest Rate],'Date Table'[Date]))

MOM AVERAGE Interest Rate:3.5%
MOM Average Interest Rate = ([MTD Average Interest Rate] - [PMTD Average Interst Rate])/[PMTD Average Interst Rate]


Good Loan Issued

For this we have created a group of loan_status attribute where good loan was accompanied by current and fully paid and bad loan with charged off  


![Good Loan issued](https://github.com/aarzoo-collab/Financial-Loan-/assets/173943221/e528509b-097d-489f-bcc3-1db80dd9b857)

Bad Loan Issued
![Bad Loan Issued](https://github.com/aarzoo-collab/Financial-Loan-/assets/173943221/78eba3a1-1798-4639-a272-c6c18239cf18)

Loan Status with 4 KPI 
![Loan Status](https://github.com/aarzoo-collab/Financial-Loan-/assets/173943221/962a097a-e76a-47c1-a866-3bf9e333dc8f)




Overview: 4 KPI ARE THERE ON OVERVIEW PAGE
TOTAL LOAN APPLICATIONS
TOTAL FUNDED AMOUNT
TOTAL AMOUNT RECEIVED
AVERAGE INTEREST RATE




4 Different Filters
Selected Measure that is a parameter 
Select Measure = {
    ("Total Loan Applications", NAMEOF('financial_loan'[Total Loan Applications]), 0),
    ("Total Funded Amount", NAMEOF('financial_loan'[Total Funded Amount]), 1),
    ("Total Amount Recieved", NAMEOF('financial_loan'[Total Amount Recieved]), 2)
} 
Term,Purpose,Grade

Total Loan Applications by Month:
Applications show an increasing trend from January to December, peaking in December at approximately 4,000 applications.

Total Loan Applications by Verification Status:
Majority of loans are “Not Verified” (blue portion in the pie chart).

Total Loan Applications by Purpose:
Most common purposes for loan applications:
‘Debt’
‘Other’
‘Business’
‘Home Improvement’
‘Auto’

Total Loan Applications by Home Ownership:
More renters apply for loans than homeowners.
Total Loan Applications by Employment Length:
Individuals employed for 10+ years have applied for the most



