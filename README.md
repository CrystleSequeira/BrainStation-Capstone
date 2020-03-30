# BrainStation-Capstone

Project: Predict wine scores from a wine review dataset that was downloaded from Kaggle. 

https://www.kaggle.com/zynicide/wine-reviews
---------------------------------------------------------

#### Python Packages needed to install: 
- conda install -c anaconda joblib
- conda install -c anaconda nltk
- conda install -c conda-forge xgboost
- conda install -c conda-forge geopy (Note: Did not end up using this package, but if you want to try to extract Latitude and Longitude as Features, you can use this package)

#### Data Folder 
- dummy_train.csv: this file is the dummy variables for variety, country, province from the train dataset. This file is important for making sure that future datasets contain the same features as the train dataset.
- train_clean.csv: Train dataset where missing values have been removed, and non essential columns are dropped.
- test_clean.csv: Test dataset after cleaning from Part 1 Jupiter notebook
- model_train.csv: Train dataset that is ready for fitting a model
- model_test.csv: Test dataset that is ready for fitting a model

#### Machine Learning Model:
logreg_ml.pkl (Best performing model - Logistic Regression)

#### Jupyter Notebooks:
Part1_Clean_Wine_Reviews.ipynb - Jupyter Notebook used for cleaning the dataset which includes Missing Values, Drop Columns, and Feature Engineering

Part2_NLP_Wine_Reviews.ipynb - Jupyter Notebook used for processing the text dataset into numerical values with NLP

Part3A_ML.ipynb - include Logistic Regression, Random Forest, and xgboost. This notebook is mainly to show previous workflow and the process of multiple iterations.

Part3B_ML_v1.ipynb - Machine Learning with final approach using Random Forest

Part3B_ML_v2.ipynb - Machine Learning with final approach using Logistic Regression and XGBoost
