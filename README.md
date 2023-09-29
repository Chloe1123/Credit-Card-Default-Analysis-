# Credit Card Default Analysis 🌟

## Abstract 📘
This project executes an in-depth analysis and develops models focusing on the components influencing credit card default. It applies the Random Forest algorithm to create a risk categorization model and identifies the crucial features impacting user default. Constructs a credit risk scorecard model based on Logistic Regression and tests the stability.

## Goal 🎯
To identify the credit risk of individual customers from the collected user default dataset to help commercial banks mitigate potential risks.

## Key Topics 🗝️
- Exploratory Data Analysis (EDA)
- Random Forest Algorithm
- Cross-Validation
- Grid Search
- Data Binning
- WOE Encoding
- Information Value
- Logistic Regression
- Credit Risk Scorecards
- Population Stability Index

## Contents 📝

### Task 1 - Exploratory Data Analysis (EDA):

Summarize the main characteristics of variables by statistical methods and visualizations, distinguishing default and non-default users across multiple dimensions.

### Task 2 - Random Forest Classification Model:

This is a binary classification task aimed at differentiating between defaulting **(default=1)** and non-defaulting **(default=0)** users and identifying the primary features that impact user default.

**Data Standardization:**
  
- Maintaining categorical variables while continuous variables are standardized to the same scale for analysis.
  
**Model Construction:**

-	Aiming for a model with optimal predictive performance, model parameters are tuned using GridSearchCV with a focus on maximizing the AUC (Area Under the ROC Curve), ensuring a balance between model complexity and generalization error. 
-	K-fold cross-validation is used to partition the data into training and test sets to mitigate estimation bias. 
-	The model is evaluated through metrics like precision, recall, F1-score, true positive rate, and false positive rate, drawn from the confusion matrix.


  
**Feature Importance:**
- The importance of each feature is computed, identifying age as the most influential factor, followed by working hours, living duration, and income. These findings align well with previous research and empirical studies on default influencing factors.


### Task 3 - Logistic Regression Credit Scorecard:

This part presents a Credit Scorecard based on Logistic Regression that assesses the risk of each loan applicant through a discriminant indicator. This model is a vital instrument for loan institutions, offering them to rate and discern the reliability of customers in various loaning environments. 
  
**Multicollinearity Test**
  
- To detect and mitigate distortions in regression coefficient estimates due to high correlation between independent variables.

**Variable Binning**

- Data adapted binning(Supervised): Discretizate Numerical Variables into defined set intervals.
- WOE (Weight of Evidence) encoding: Convert nonlinear features to linear.

**Variable Selection:**
  
- Utilizing Information Value (IV) to measure the predictive power of independent variables.
  
**Logistic Regression:**

- Using 5-fold cross-validation with a penalty and a regularization coefficient to prevent overfitting and refine the model's predictive accuracy.
  
**Score-Points Scaling:**

- Establishing the base score, Odds, PDO, and points to each binned variable.
  
**Stability Evaluation:**
  
- Using the Population Stability Index (PSI) to indicate model stability.
