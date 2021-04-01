# Loan Data Exploration
## by Marina Atef


## Dataset

> after cleaning dataset there are 58,539 loans in the dataset with 13 features (Term ,LoanStatus ,BorrowerRate ,LenderYield ,ProsperScore,ListingCategory (numeric),EmploymentStatus,LoanOriginalAmount,EstimatedLoss,EstimatedReturn,IncomeVerifiable). Most variables are numeric in nature and the variables LoanStatus , Occupation and EmploymentStatus is object datatype but ProsperScore and Term are ordered variable with the following levels.
ProsperScore : 1 , 2 , 3 ... , 10
Term : 12 , 36 , 60


## Summary of Findings

first my numaric features not in the same range so I don't need to perform any transformations on BorrowerAPR ,BorrowerRate,ProsperScore,EstimatedLoss,EstimatedReturn and LenderYield because they took on a smalle range of values,  but i do in loans amount .

then I split Loan Status to put types of PastDue in one category and name it as PastDue and clean the data from null values and start in exploration.

In the exploration, I found that there is a highly correlation between loan's  amount with term and ProsperScore has high correlation with loan's amount also if your Employment state is ('Employed' , 'Self-employed') , then your loan amount is bigger than other Employment statuses.

Estimated Loss and Estimated Return are highly correlated with lenderYield and BrroweRate  but they have negative corrolation with loan's amount.

the  'Borrowing Rate', and 'Lender Yield'  are  highly correlated with one another


you can see the relationship of 'EstimatedReturn' against 'BorrowerRate' and 'LoanStatus', we can see that most current state in rang of lender Yield  from zero to 0.2 and Estimated Return from zero to 0.10 but PastDue most of them in range more than 0.2 for lender Yield and  0.10 for Estimated Return so it is incresed when Estimated Return and lender Yield are increse ,also final payment state is increased when Estimated Return and lender Yield are increased but has longer range than pastdue state.

finally loans in ('Current' , 'PastDue' , 'FinalPaymentinProgress') are high in 'Prosper Score' and Personal Loan also has zero in 'Prosper Score'.

## Key Insights for Presentation

For the presentation, I just focus on relationship between Borrower Rate ,Estimated Return and loan's state and leave out most of the features

on another hand thier is high corralation between EstimatedLoss and Estimated Return also a high corralation between Borrower Rate and Lender Yield

I start by introducing the
LoanStatus variable, followed by the pattern in LoanOriginalAmount distribution in log transformed scatterplot.

then I introduce each of the interested variables one by one .

finally I introduce correlation matrix and using faceted heat maps
to introduce relationship between Estimated Return against Borrower Rate and LoanStatus which help us to understand alot things.
