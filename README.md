# Data-Science-Series
For all those who're struggling to find a good hands-on resource (with case studies) to master their Data Science skills, Here's all what you need!


## CONCEPT 1: Exploratory Data Analysis

### Credit Risk Modeling Case Study

#### Problem Statement:
ABC Finance Company is finding it hard to give loans to the people due to their insufficient or non-existent credit history. Because of that, some consumers use it as their advantage by becoming a defaulter. Suppose you work for ABC finance company which specializes in lending various types of loans to urban customers. You have to use EDA to analyze the patterns present in the data. This will ensure that the applicants are capable of repaying the loan are not rejected.
When the company receives a loan application, the company has to decide for loan approval based on the applicant’s profile. Two types of risks are associated with the bank’s decision:
•	If the applicant is likely to repay the loan, then not approving the loan results in a loss of business to the company.
•	If the applicant is not likely to repay the loan, i.e. he/she is likely to default, then approving the loan may lead to a financial loss for the company. 
The bank wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default 

#### Now, what should you do?

Identify patterns which indicate if a client has difficulty paying their installments which may be used for taking actions such as denying the loan, reducing the amount of loan, lending (to risky applicants) at a higher interest rate, etc. This will ensure that the consumers capable of repaying the loan are not rejected. Identification of such applicants using EDA is the aim of this case study. 
In other words, the company wants to understand the driving factors (or driver variables) behind loan default, i.e. the variables which are strong indicators of default. The company can utilize this knowledge for its portfolio and risk assessment.
To develop your understanding of the domain, you are advised to independently research a little about risk analytics - understanding the types of variables and their significance should be enough).

#### Datasets:

1. 'application_data.csv' contains all the information of the client at the time of application. The data is about whether a client has payment difficulties.
2. 'previous_application.csv' contains information about the client’s previous loan data. It contains the data whether the previous application had been Approved, Cancelled, Refused or Unused offer.

Datasets uploaded here: https://drive.google.com/drive/folders/1IWQBgaO8e_VDi6GBnluLJTlOQFSTPtcL?usp=sharing

Note: You can refer to Columns description file to learn about the columns available in the datasets.


#### *How to begin?* 

1.	Start by importing the 'application_train.csv'. 

2.	Check the structure of the data (shape, info, describe). 

3.    Data Quality Check and Missing values 

a. Find the percentage of missing values for all the columns. 

b. Remove columns with high missing percentage. 

c. For columns which has less percentage (around 13% or so), you need to check what will be the best metric to impute the missing values? Like if the column you are    checking is a categorica column check, which category you can use to fill the nulls. For others check does mean or median can be imputed or not. Other cases may    be imputing with 0. You need to do this task for some variables and not for all, say 5.

4.	Check the datatypes of all the columns and change the datatype if required. 

5.	For numerical columns check for outliers and report them for at-least 3 variables. Treat them and analyze it. 

6.	Binning of continuous variables. Check if you need to bin any variable in different 
categories. Do this for one or two columns. 


#### *Analysis Steps*

1.	Check the Imbalance percentage. No balancing technique required. 

2.	Divide the data into two sets, i.e. Target=1 and Target=0. 

3.	Perform univariate analysis for categorical variables for both 0 and 1. Compare the target variable across categories of categorical variables. 

4.	Find correlation for numerical columns for both the cases, i.e. 0 and 1. 

5.	Check the variables with highest correlation are the same in both the files or not? 

6.	Perform univariate for numerical variables for both 0 and 1. Compared the target variable across categories of continuous variables.

7.	Perform bivariate analysis for numerical variables for both 0 and 1. 

8.	Read “Previous Application” data. 

9.	Merge the files

10.	Perform univariate and bivariate analysis to find some pattern. 


## CONCEPT 2: Multiple Regression

![LinearRegression](https://github.com/gitsuraaj/Data-Science-Series/blob/master/Pictures/5-Step-Workflow-for-Multiple-Linear-Regression.png)

### YuluDulu Bicycle Subscription Case Study
 
#### Problem Statement
A bike-sharing provider YuluDulu has recently suffered considerable dips in their revenues. They have contracted a consulting company to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know: 
•	Which variables are significant in predicting the demand for shared bikes?
•	How well those variables describe the bike demands 

#### What you need to do? 
•	Create a linear model that describe the effect of various features on price. 
•	The model should be interpretable so that the management can understand it. 
  

#### Case Study Steps to be performed

#### *Data Preparation*

1.	Identify the categorical and continuous features. 
2.	Drop the unnecessary variables: ‘instant’, ‘dteday’, ‘casual’ and ‘registered’. 
3.	Check the data-type of all the columns and make necessary changes if required. 

#### *Data Visualization*

4.	Perform EDA to understand various variables. 
5.	Check the correlation between the variables. 

#### *Data Preparation*

6.	Create dummy variables for all the categorical features. 
7.	Divide the data to train and test. 
8.	Perform scaling. 
9.	Divide the data into X and y. 

#### *Data Modelling and Evaluation* 

10.	Create Linear Regression model using mixed approach. 
11.	Check the various assumptions. 
12.	Check the Adjusted R-Square for both test and train data. 
13.	Report the final model. 

#### Data set “YuluDulu Dataset.csv” and its description “YuluDulu Columns Description” is uploaded in the same folder.


## CONCEPT 3: Supervised Learning through Classification

### Potential Customers for X Education
An education company named X Education sells online courses to industry professionals. The company markets its courses on several websites and search engines like Google. Once these people land on the website, they might browse the courses or fill up a form for the course or watch some videos. When these people fill up a form providing their email address or phone number, they are classified to be a lead. Now, although X Education gets a lot of leads, its lead conversion rate is very poor. For example, if, say, they acquire 100 leads in a day, only about 30 of them are converted. 

#### What you need to do? 
•	X Education has appointed you to help them select the most promising leads, i.e. the leads that are most likely to convert into paying customers. 
•	The company requires you to build a model wherein you need to assign a lead score to each of the leads such that the customers with higher lead score have a higher conversion chance and the customers with lower lead score have a lower conversion chance. 
Steps to follow:

#### Data Cleaning 
•	Handle the “Select” level that is present in many of the categorical variables. 
•	Drop columns that are having high percentage of missing values. Check all the columns before dropping them. 
•	Check the number of unique categories in each categorical column. Here you may need to do something. 
•	For the columns with less percentage of missing, use some imputation technique. 
•	Finally check the percentage of rows retained in data cleaning process. 

#### Data Preparation 
•	Create dummies for all categorical columns. 
•	Perform train-test split. 
•	Perform scaling. 

#### Modelling
•	Use techniques like RFE to perform variable selection. 
•	Build a Logistic Regression model with good sensitivity. 
•	Check p-value and VIF. 
•	Find the optimal probability cutoff. 
•	Check the model performance over the test data. 
•	Generate the score variable. 


