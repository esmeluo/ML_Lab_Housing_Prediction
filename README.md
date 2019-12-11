# 2019 Machine Learning Lab

## Objectives

Utilize the tool set we've learned in Machine Learning Lab to make an accurate prediction of Housing prices.

## Folders

* Data: Contains source data we gathered from kaggle
* Final Presentation: Final Presentation Notebook and pdfs (Deliverable)
* Graphs: EDA graphs generated and linked in the presentation.
* Notebooks: 
  * Housing_Sale_Price_Prediction.ipynb (Final Deliverable)

## Workflow

* Packages Required
  * Pandas
  * Sklearn

* Data Preprocessing
  * Gain a high level understanding of the data using Pandas_Profiling package.
  * Based on the information gathered, we decided to drop data with large % of null values to avoid introducing bias to the model.
  * Dropped Categorical data with too many classes (Data would be too sparse and creates too many column, not enough observation for training).
  
* Exploratory Data Analysis

  * Correlation Analysis
    Multicolinearity issues identified amongst variables. (i.e 1st floor sqft, 2nd floor sqft)
    
  * Analysis of Response Distribution 
    Log transformation performed on response to normalize target distribution.
  
* Feature Selection
  * Naive selection - selection includes squarefeet, neiborhood and housestyle, year built based on intuition.
  * Full Model - all features included.
  * Reduced Model - feature removed based on permutation importance score.

* Modelling Approach
  * Linear Regression (Lasso)
  * Random Forest Regressor
  * Gradient Boosting Regressor

* Evaluation Metrics
  * MAE, MSE, MAPE, RLMSE
  * We've decided to use RLMSE as our final choice of evaluation

*  Final Choice of Model
  * Random Forest Regressor
  * Reasoning: 
    * Best performing model based on RLMSE
    * Minimal overfitting compared to Gradient Boosting Regressor
  * Hyperparameters: n_estimators=12, min_samples_split=7, max_features=39, max_depth=None, bootstrap=True
 
  

  
  
  

