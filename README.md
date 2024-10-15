CONTEXT:  A bank X is on a massive digital transformation for all its departments. Bank has a growing customer base whee  majority of them are liability customers (depositors) vs borrowers (asset customers). The bank is interested in expanding the  borrowers base rapidly to bring in more business via loan interests. A campaign that the bank ran in last quarter showed an  average single digit conversion rate. Digital transformation being the core strength of the business strategy, marketing  department wants to devise effective campaigns with better target marketing to increase the conversion ratio to double digit  with same budget as per last campaign.

DATA DICTIONARY:

ID: Customer ID
Age: Customer’s approximate age.
CustomerSince: Customer of the bank since. [unit is masked]
HighestSpend: Customer’s highest spend so far in one transaction. [unit is masked]
ZipCode: Customer’s zip code.
HiddenScore: A score associated to the customer which is masked by the bank as an IP.
MonthlyAverageSpend: Customer’s monthly average spend so far. [unit is masked]
Level: A level associated to the customer which is masked by the bank as an IP.
Mortgage: Customer’s mortgage. [unit is masked]
Security: Customer’s security asset with the bank. [unit is masked]
FixedDepositAccount: Customer’s fixed deposit account with the bank. [unit is masked]
InternetBanking: if the customer uses internet banking.
CreditCard: if the customer uses bank’s credit card.
LoanOnCard: if the customer has a loan on credit card.
PROJECT OBJECTIVE: Build a Machine Learning model to perform focused marketing by predicting the potential customers who will convert using the historical dataset.

STEPS AND TASK [30 Marks]:

Data Understanding and Preparation: [5 Marks]
Read both the Datasets ‘Data1’ and ‘Data 2’ as DataFrame and store them into two separate variables. [1 Marks]
Print shape and Column Names and DataTypes of both the Dataframe. [1 Marks]
Merge both the Dataframe on ‘ID’ feature to form a single DataFrame [2 Marks]
Change Datatype of below features to ‘Object’ [1 Marks] * [‘CreditCard’, ‘InternetBanking’, ‘FixedDepositAccount’, ‘Security’, ‘Level’, ‘HiddenScore’]
[Reason behind performing this operation:- Values in these features are binary i.e. 1/0. But DataType is ‘int’/’float’ which is not expected.]
Data Exploration and Analysis: [5 Marks]
Visualize distribution of Target variable ‘LoanOnCard’ and clearly share insights. [2 Marks]
Check the percentage of missing values and impute if required. [1 Marks]
Check for unexpected values in each categorical variable and impute with best suitable value. [2 Marks]
[Unexpected values means if all values in a feature are 0/1 then ‘?’, ‘a’, 1.5 are unexpected values which needs treatment]
Data Preparation and model building: [10 Marks]
Split data into X and Y. [1 Marks]
[Recommended to drop ID & ZipCode. LoanOnCard is target Variable]
Split data into train and test. Keep 25% data reserved for testing. [1 Marks]
Train a Supervised Learning Classification base model - Logistic Regression. [2 Marks]
Print evaluation metrics for the model and clearly share insights. [1 Marks]
Balance the data using the right balancing technique. [2 Marks]
Check distribution of the target variable
Say output is class A : 20% and class B : 80%
Here you need to balance the target variable as 50:50.
Try appropriate method to achieve the same.
Again train the same previous model on balanced data. [1 Marks]
Print evaluation metrics and clearly share differences observed. [2 Marks]
Performance Improvement: [10 Marks]
Train a base model each for SVM, KNN. [4 Marks]
Tune parameters for each of the models wherever required and finalize a model. [3 Marks]
(Optional: Experiment with various Hyperparameters - Research required)
Print evaluation metrics for final model. [1 Marks]
Share improvement achieved from base model to final model. [2 Marks]
