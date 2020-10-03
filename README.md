# Problem statement

## Context 
Banks offer credits, which can be considered as short- and long-term investments with their own risks. Sometimes client can delay payments or even stop paying at all. Latter situation is called 'default' can result in monetary losses for the bank. To avoid clients that might default banks hire credit officers that evaluate each client, based on the available data. Some banks prefer using credit scorecards, which contain simple classification of the clients to predict the probability of default. However, such scorecards are usually developed utilizing inferior methods. In this porject I try to develop credit scorecard and model that can automatically evaluate each client faster than any credit officer.

## Goals
* Build model with acceptable precision and recall.
* Find best predictor factors of the default.
* Make a credit scorecard and prepare it for implementation.


# Data exploration

## Data source
Original dataset, in the form provided by Prof. Hofmann, was downloaded from [UCI Irvine Machine Learning Repository.](https://archive.ics.uci.edu/ml/datasets/statlog+(german+credit+data))

## Data description
Number of Instances:  1000

Attribute 1:  (qualitative)
	      * Status of existing checking account
          * A11 :      ... <    0 DM
	      * A12 : 0 <= ... <  200 DM
	      * A13 :      ... >= 200 DM / salary assignments for at least 1 year
          * A14 : no checking account

Attribute 2:  (numerical)
          * Duration in month

Attribute 3:  (qualitative)
	      * Credit history
	      * A30 : no credits taken/all credits paid back duly
          * A31 : all credits at this bank paid back duly
	      * A32 : existing credits paid back duly till now
          * A33 : delay in paying off in the past
	      * A34 : critical account/other credits existing (not at this bank)

Attribute 4:  (qualitative)
	      * Purpose
	      * A40 : car (new)
	      * A41 : car (used)
	      * A42 : furniture/equipment
	      * A43 : radio/television
	      * A44 : domestic appliances
	      * A45 : repairs
	      * A46 : education
	      * A47 : (vacation - does not exist?)
	      * A48 : retraining
	      * A49 : business
	      * A410 : others

Attribute 5:  (numerical)
	      * Credit amount

Attibute 6:  (qualitative)
	      * Savings account/bonds
	      * A61 :          ... <  100 DM
	      * A62 :   100 <= ... <  500 DM
	      * A63 :   500 <= ... < 1000 DM
	      * A64 :          .. >= 1000 DM
          * A65 :   unknown/ no savings account

Attribute 7:  (qualitative)
	      * Present employment since
	      * A71 : unemployed
	      * A72 :       ... < 1 year
	      * A73 : 1  <= ... < 4 years  
	      * A74 : 4  <= ... < 7 years
	      * A75 :       .. >= 7 years

Attribute 8:  (numerical)
	      * Installment rate in percentage of disposable income

Attribute 9:  (qualitative)
	      * Personal status and sex
	      * A91 : male   : divorced/separated
	      * A92 : female : divorced/separated/married
          * A93 : male   : single
	      * A94 : male   : married/widowed
	      * A95 : female : single

Attribute 10: (qualitative)
	      * Other debtors / guarantors
	      * A101 : none
	      * A102 : co-applicant
	      * A103 : guarantor

Attribute 11: (numerical)
	      * Present residence since

Attribute 12: (qualitative)
	      * Property
	      * A121 : real estate
	      * A122 : if not A121 : building society savings agreement/life insurance
          * A123 : if not A121/A122 : car or other, not in attribute 6
	      * A124 : unknown / no property

Attribute 13: (numerical)
	      * Age in years

Attribute 14: (qualitative)
	      * Other installment plans 
	      * A141 : bank
	      * A142 : stores
	      * A143 : none

Attribute 15: (qualitative)
	      * Housing
	      * A151 : rent
	      * A152 : own
	      * A153 : for free

Attribute 16: (numerical)
          * Number of existing credits at this bank

Attribute 17: (qualitative)
	      * Job
	      * A171 : unemployed/ unskilled  - non-resident
	      * A172 : unskilled - resident
	      * A173 : skilled employee / official
	      * A174 : management/ self-employed/highly qualified employee/ officer

Attribute 18: (numerical)
	      * Number of people being liable to provide maintenance for

Attribute 19: (qualitative)
	      * Telephone
	      * A191 : none
	      * A192 : yes, registered under the customers name

Attribute 20: (qualitative)
	      * Foreign worker
	      * A201 : yes
	      * A202 : no
          
Attribute 21: (qualitative)
          * Evaluation of the customer
          * (1 = Good,  2 = Bad)

# Visualizations

![](https://github.com/aza-atabayev/credit_scorecard/blob/master/images/1.png?raw=true)
![](https://github.com/aza-atabayev/credit_scorecard/blob/master/images/2.png?raw=true)
![](https://github.com/aza-atabayev/credit_scorecard/blob/master/images/3.png?raw=true)

# Conclusion

* Model with the accuracy of 77.63% was developed
* Threshold of 300 credit points was found to be the most efficient
* The best predictors of bad/good credits are money on the current account, amount of credit, duration of the credit period, age of the customer, history of paying the credits, money on the savings account.
