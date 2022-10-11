# Loan-Approval-Classification-with-imbalanced-data

##About Dataset

Should This Loan be Approved or Denied?

The Small Business Administration (SBA) was founded in 1953 to assist small businesses in obtaining loans. Small businesses have been the primary source of employment in the United States. Helping small businesses help with job creation, which reduces unemployment. Small business growth also promotes economic growth. One of the ways the SBA helps small businesses is by guaranteeing bank loans. This guarantee reduces the risk to banks and encourages them to lend to small businesses. If the loan defaults, the SBA covers the amount guaranteed, and the bank suffers a loss for the remaining balance.

There have been several small business success stories like FedEx and Apple. However, the rate of default is very high. Many economists believe the banking market works better without the assistance of the SBA. Supporter claim that the social benefits and job creation outweigh any financial costs to the government in defaulted loans.

##The Data Set

The original data set is from the U.S.SBA loan database, which includes historical data from 1987 through 2014 (899,164 observations) with 27 variables. The data set includes information on whether the loan was paid off in full or if the SMA had to charge off any amount and how much that amount was. The data set used is a subset of the original set. It contains loans about the Real Estate and Rental and Leasing industry in California. This file has 2,102 observations and 35 variables. The column Default is an integer of 1 or zero, and I had to change this column to a factor.

For more information on this data set go to https://amstat.tandfonline.com/doi/full/10.1080/10691898.2018.1434342

## Project Description
I have done two seperate modeling of the project. Below are the descriptions of both works.


### Initial Baseline Models Logistic regression and Decision Tree classifier

Project Starter - Simple Baseline Logistic and Decision Tree Models include following tasks

- Load dataset
- Clean up the data:
    - Encode replace missing values
    - Replace features values that appear incorrect
- Encode categorical variables
- Split dataset to Train/Test/Validation
- Add engineered features
- Train and tune ML model
- Provide final metrics using Validation dataset

 As part of your deliverables, I will be create scoring function. The scoring function will perform following:
- Accept raw dataset in the same format as provided in Kaggle dataset, minus "MIS_Status" column
- Load trained model and any encoders that are needed to transform data
- Transform dataset into format that can be scored with the trained model
- Score the dataset and return the results, for each record
    - Record ID
    - Record label as determined by final model (0 or 1)
    - If the model returns probabilities, assign label based on maximum F1 threshold


Deliverables:
- Jupyter notebook with complete code to manipulate data, train and tune final model
- Model and any potential encoders in the "pkl" format
- Scoring function that will load final model and encoders


The notebook includes explanations about the code and is designed to be easily followed and results replicated.

### Final Model with Ensenble Learning

In this project, we are not using the "Term" feature which is the most important feature based on the initial analysis with simpler models. The reason is to avoid the model to be more dependent on this feature and not learn the others. I will add the "Term" feature at the end to find the overall progress with and without this feature. The notebook includes the following tasks.

- Clean up the data:
    - Encode replace missing values
    - Replace features values that appear incorrect
- Encode categorical variables
- Split dataset to Train/Test/Validation
- Add engineered features
- Train and tune ML model (LightGBM Gradient Boosting / DART (dropout additive regression trees))
- Explain and interpret model results, feature importances, contirbutions (Permutation importance, Shap contribution)
- Residual analysis
- Provide final metrics using Validation dataset

 Deliverables are the same as the deliverables of the first model.

Overall Performance: F1 score of 0.95.
