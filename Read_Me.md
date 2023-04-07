
# Loan Default
![image](https://user-images.githubusercontent.com/45716414/228026912-5111c67d-db6b-4aec-89ca-e28eb51c9e71.png)

# Business Understanding:
Banks face significant losses when customers default on their loans, which in turn negatively impacts the economic growth of the country. In order to address this problem, a data scientist is needed to conduct an in-depth analysis of loan data to identify the factors that influence loan defaults. The goal of this project is to develop a marketing plan that will enable banks to contact borrowers and minimize losses. To achieve this goal, we will be utilizing various data science techniques, including logistic regression, decision tree, random forest, and Xgboost. This project will be considered a binary classification problem, where we aim to identify whether a client will default on their loan or not. The insights gained from this analysis will be used to inform decision-making and mitigate losses for banks and investors while promoting economic growth.

# Steakholder: Chase Consumer Bank

# Business Problem: 
Will our clients default on their loan or not?


In the context of developing a marketing plan to minimize losses for the bank, the focus should be on reducing the number of false positives or Type 1 errors.

This is because false positives occur when the model predicts that a borrower will default on their loan when they actually will not. If the bank were to contact all borrowers who were predicted to default (i.e., all positive instances), including those who will not actually default, it would result in unnecessary costs for the bank and may also damage the bank's relationship with borrowers who are able to repay their loans.

Therefore, in order to minimize losses, it is important to focus on reducing the number of false positives or Type 1 errors. This can be achieved by improving the precision of the loan default prediction model, so that the model only identifies borrowers who are highly likely to default. By doing so, the bank can focus its resources on contacting the borrowers who are most likely to default, while minimizing the cost of unnecessary contact with borrowers who will not default.

# Data Understanding:
https://www.kaggle.com/datasets/hemanthsai7/loandefault?resource=download

MachineHack has created a training dataset of 67,463 rows and 35 columns and a testing dataset of 28,913 rows and 34 columns. 

`ID` - unique identifier for each loan application

`Loan Amount` - the amount requested by the borrower

`Funded Amount` - the amount funded by investors for the loan

`Funded Amount Investor` - the amount funded by investors for the loan

`Term` - the length of the loan term in months

`Batch Enrolled` - the batch enrollment method for the loan

`Interest Rate` - the interest rate on the loan

`Grade` - the Lending Club assigned loan grade

`Sub Grade` - the Lending Club assigned loan subgrade

`Employment Duration` - the employment length of the borrower

`Home Ownership` - the type of home ownership of the borrower

`Verification Status` - indicates if the borrower’s income was verified

`Loan Title` - the title of the loan as provided by the borrower

`Debit to Income` - the borrower’s debt-to-income ratio

`Delinquency - two years` - the number of times the borrower has been delinquent in the past two years

`Inquires - six months` - the number of inquiries made on the borrower’s credit in the past six months

`Open Account` - the number of open credit lines in the borrower's credit file

`Public Record` - the number of derogatory public records on the borrower's credit file

`Revolving Balance` - the balance on the borrower's revolving credit accounts

`Revolving Utilities` - the amount of the borrower's revolving credit that is currently in use

`Total Accounts` - the total number of credit lines the borrower has

`Initial List Status` - the initial listing status of the loan

`Total Received Interest` - total interest received to date

`Total Received Late Fee` - total late fees received to date

`Recoveries` - post charge off gross recovery

`Collection Recovery Fee` - post charge off collection fee

`Collection 12 months Medical` - number of collections in medical categories in the last 12 months

`Application Type` - indicates whether the loan is an individual or joint application

`Last week Pay` - the last week’s payment on the loan

`Total Collection Amount` - total amount due after the charged off

`Total Current Balance` - total current balance of all accounts

`Total Revolving Credit Limit` - total revolving credit limit

`Loan Status` - current status of the loan

`Debt-to-Income Ratio` - the borrower's debt-to-income ratio

`Credit Utilization Ratio` - the borrower's credit utilization ratio

`Time Since Last Delinquency` - the number of months since the borrower's last delinquency

# Methods: For this binary classification problem the two classes were labeled 0 = not in default and 1 = in default

Data preprocessing and cleaning techniques (feature scaling, encoding categorical variables)

Data exploration and visualization methods

Model selection and evaluation techniques (e.g., train/test split, cross-validation, hyperparameter tuning)

Classification models used (e.g., logistic regression, decision trees, random forest, XGBoost)

Performance metrics used to evaluate the models (e.g., accuracy, precision, recall, F1 score, AUC-ROC)

# Results: 
### Baseline Logistic Regression:
![image](https://user-images.githubusercontent.com/45716414/228037848-df604e47-bfd4-4e1e-8e5c-dc95c04ea0f5.png)


### XGBoost Hypertuned:
![image](https://user-images.githubusercontent.com/45716414/228036896-a65b7cc9-6469-412a-9a05-a3e0a82d9a8e.png)


# Limitations and Further Analysis
Limitations:

* Our models were better at predicting the majority class (not in default) than our minority class(in default) even though we used random oversampling to addrress thee clcass imbalannce. It is poossible that we could improve perfomance by trying other oversampling techniques such as SMOTE (Synthetic Minority Over-sampling Technique) or ADASYN (Adaptive Synthetic Sampling). We could have also looked into using undersampling techniques such as Random undersampling, Tomek links, and Cluster centroids

* The data used for the analysis may not be representative of the current market or economic conditions. The analysis was conducted on a historical dataset, and the default patterns and risk factors could have changed since then.

* The model may suffer from selection bias if the loan applicants in the dataset are not representative of the entire population. For example, the dataset may contain a disproportionate number of applicants with high credit scores, which could skew the model's predictions.

* The model assumes that the predictors are independent of each other, which may not always be the case. For example, the applicant's income and employment status may be correlated, and the model may not capture this relationship accurately.



Further analysis:

* Conducting a cost-benefit analysis to evaluate the economic impact of the model's predictions. This analysis could help determine the optimal threshold for classifying loans as default or non-default and inform decisions on lending policies and risk management.

* Exploring additional data sources or features that could improve the model's predictive power. For example, incorporating macroeconomic indicators or social media data could provide insights into broader economic trends and consumer sentiment.

* Experimenting with different feature selection and engineering techniques: This can help identify the most relevant features for the model and improve its accuracy.


* Investigating the reasons behind loan defaults and developing targeted interventions to reduce default rates. For example, offering financial education or counseling to high-risk borrowers could improve their financial literacy and ability to repay loans.

