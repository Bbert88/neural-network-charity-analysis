# Analysis of Organizations funding successes using neural networks

## Overview

The purpose of this analysis is to create a binary classifier that is capable of predicting whether applicants will be successful if they are funded. The dataset which was provided included records of approx. 34,000 organizations that have received funding over recent years. This was completed by designing machine learning models using neural networks. I created several models and evaluated them for accuracy. I then optimized the model to try and increase their accuracy.

## Results

### Data Preprocessing

- The target variable for this dataset is the "IS_SUCCESSFUL" column. This feature reads "0" or "1", which represent if the organization which received the funding was successful or not.
- Features: The features for the model are as follows:
  - APPLICATION_TYPE—Alphabet Soup application type
  - AFFILIATION—Affiliated sector of industry
  - CLASSIFICATION—Government organization classification
  - USE_CASE—Use case for funding
  - ORGANIZATION—Organization type
  - STATUS—Active status
  - INCOME_AMT—Income classification
  - SPECIAL_CONSIDERATIONS—Special consideration for application
  - ASK_AMT—Funding amount requested
- Data removed/not useful: 
  - EIN and NAME columns which were identification columns.

### Compiling, Training, and Evaluating the Model

- The original model used 2 hidden layers with 80 and 30 neurons, respectively. The activation function used was "relu" with the output function as "sigmoid". 
- The original deep learning model did not achieve the 75% accuracy benchmark. It came in at 72.9%. 
- Steps taken to try and increase model performance:
  - Additional variables were removed such as "ASK_AMT" due to the large variance in the numerical values which could be deemed as "noisy". 
  - An additional hidden layer was added. 
  - The number of neurons was increased in each hidden layer. 
  - The activation was changed to "tanh" and "sigmoid"

## Summary

Despite all of the attempts made at optimizing the model, the accuracy did not reach 75%. Perhaps a different model could provide better results due to the characteristics of the data. A Support Vector Machine could produce a higher accuracy level as it is also a supervised learning method used for classification. SVMs are highly effective in high dimensional spaces, which this dataset could be classified as. 