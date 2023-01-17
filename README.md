# Exploring The Prosper Loan Dataset
## A Udacity Nano-degree project

## Dataset Overview:

The dataset consist of 113937 rows and 81 columns of loans records measuring loans performance for the period between 2009 and 2016. 
The records hold data such as loan amount, borrower rate (or interest rate), loan status, borrower income, delinquencies, loan terms etc. The term of the loan is expressed in months, delinquency is measured as pure count and stored in two seperate features that measure for current and the previous seven years delinquencies. Overall, each variable hold information as at the time the loan originated or the loan records was pulled.

This exploration identifies the delinquency variable, `DelinquenciesLasst7years` as target, and will focus on understanding how the target associates with select features of the dataset. The  target measures delinquencies per loan accounts for a period of seven years. Other variables considered alongside the target measures or indicates: rate, original loan amount, income range, loan status, employment status, income to debt ratio, and occupation. 

Initial feature selection will be fairly large in the wrangling stage to allow for better understanding of the dataset. Subsequent and final feature selections will be carried out in the variable analysis phase to investigate for distributions and possible association amongst the variables, with emphasis on the target. However, where needed, variables may be introduced intermittently or engineered to further the analysis.



## Summary of Findings:

A three-phased analysis was performed during the exploration: Univariate, Bivariate, and Multivariate analyses were carried out to understand the distribution and relationships that exist amongst variables. In order to do so, data transformations were performed, where necessary, to normalized distribution. Methods used include Logarithm, Square-root, and Box-Cox transformations. The target variable, `DelinquenciesLast7Years`, which measures delinquency, was examined for its distribution and correlation with predictor variables. 
The following observations were made:
The numeric variables, including the target, were observed to be skewed to the right, except for the rate variable, “BorrowerRate”, which appeared to follow normal distribution. Transforming the variables revealed distributions with multiple peaks that appeared as clusters at various points. Further analysis found there exist 21 loan classes, and their distributions peak at point zero, 0, representing loans with no delinquencies. The loans are heavily distributed towards non-delinquency. The proportion of non-delinquent loans is evidently higher than delinquent loans and this is the case across the various categories. 
Debt-consolidation category accounts for more than 50% of the overall loan business and also has the largest proportion of non-delinquent loan accounts, approximated at 56% of non-delinquent population. Average delinquency for loans is 2.9, and delinquency can be as low as 2.2 or as high as 4.5, although, most loans tend to average 3 delinquencies. Only 24% of the categories; medical/dental, boat, home-improvement, engagement-ring, and the class “other”, exhibited delinquencies below the average point: motorcycle 2.75, student_use2.43, personal 2.39, baby adoption 2.38, and green-loans 2.22.



From relationship standpoint, we observed as follows:

The numeric predictors exhibited mostly negative correlation against the target except for rate variable, BorrowerRate, which associated positively with the target. Delinquency decreases as yearly-income, debt-to-income ratio, loan-original-amount; each, increases. 
Although, rate exhibited a strong positive linear relationship with delinquency, it does not imply that it causes delinquency. The introduction of categorical variables; loan-status, employment-status, debt-to-income-ratio, and income-bracket variables varied rate/delinquency relationship across the categorical variables' classes. 
This observation was evident when rate/delinquency relationship was observed across income classes in multivariate analysis phase which produced a form of quadratic relationship. The two extremes of the income classes showed lower delinquency than the middle classes.
Across income classes, delinquency tend to decline as income increases. At higher borrower's rate, higher income classes `($75,000-99,999, $100,000+)` indicate significant decline in delinquency while the lower income classes `($0, $1-24,999, $25,000-49,999)` show higher proportion at higher rate.
On the other hand, the proportion and frequency with which loans with high debt-to-income ratio are delinquent tend to decline as income class increases. Loans with low or medium ratio tend to associate with higher delinquency, while those with high or very-high ratio tend to associate with low delinquency
Interestingly, higher income indicated significant delinquency at various rate points and ratio class, which lead to the conclusion that delinquency and its association with rate behave differently across the classes of income, loan status, and ratio variables. A combination of effects from multiple variables rather one, seem to be in play in for delinquency to be the case.
