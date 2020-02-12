# Loan_Models_ppd

# Project Overview
The purpose of this project was to utilize publically available credit data to evaluate the performance of several machine learning models, diagnosing strengths and weaknesses of each and make recommendations, if possible, for which one would be suitable for implementation. 

## What we are evaluating
One issue with credit data is the overwhelming imbalance between how many loans would be characterized as good (many) versus how many would be described as poor (few). The aim of the machine learning models is to accurately predict which loans should be predicted accurately (low-risk loans are predicted as low-risk and high-risk loans are accurately predicted as high-risk). With such an imbalance, it is difficult to correctly diagnose both camps with equal confidence. As a result, the aims of the oversampling and undersampling models is to consider that challenge and boost (oversample) the relatively few high-risk loans to create “proxy” high-risk loans or undersample (restrict the volume of low-risk loans) to create a level-playing field for both loan classes, per se. In the final case, a combination of both over and undersampling is performed. 
Additionally two ensemble classifiers are called to evaluate performance. Summary results and recommendations are provided in respective notebooks. 

## How we evaluate performance
Three criteria are considered when looking at model performance. 
### Accuracy
Very simply this is how accurate the model predicts outcome. The data set is columns and columns of input characteristics (job type, income level, car owner, etc.) that all determine if someone is a high or low-risk loan applicant. Model data is broken into a test class and a predicted class. Knowing what we know from the test class of applicants, we use that to develop a "formula" to predict, with a given set of inputs, what kind of loan applicant is applying. Since we already have the application classification, we compared the predicted result to the actual result. The balanced accuracy score can be thought of as how many correct guesses were made out of how many guesses were made in total.  

### Precision
This is a measure of how many high-risk (or low-risk) loans are correctly predicted. If the model predicts 100 loans to be high-risk, but only 10 are actually high-risk with the balance of being 90 low-risk loans incorrectly assumed to be high-risk. In this example, precision would be 10%

### Recall
This is a measure of how many high-risk (or low-risk) loans are correctly identified. So if there are 100 risky-loans but the model only predicts that 30 are risky with the balance identified as low-risk, then recall (or sensitivity) is 30%. 

