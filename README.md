## Use of NLP and supervised learning to predict wine scores from wine descriptions

Original dataset is taken from [Kaggle](https://www.kaggle.com/zynicide/wine-reviews)

#### Problem Statement:
Predicting how a wine will perform and understanding why that wine performs can be beneficial for consumers and sellers of wine. For example, a winemaker might want to gain insights into why their pinot noir is rated higher ¬than their chardonnay. As well, wine distributers might want to make profitable decisions like is it worth it to invest in an expensive wine and will this wine sell. To delve into these questions, I created a predictive model to target wine scores and analyzed a dataset that includes the geography of the wine, price, description, variety, and vintage.

#### Description of the dataset:
- Datatframe exported as a csv with information about wine
- Data was originally scraped from the kaggle user on www.winemag.com
- 130k rows and 12 columns

#### Methods:
1. Clean data
2. Feature Engineering
3. 
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

#### Notebook Folder:
- Part1_Clean_Wine_Reviews.ipynb - Jupyter Notebook used for cleaning the dataset which includes Missing Values, Drop Columns, and Feature Engineering
- Part2_NLP_Wine_Reviews.ipynb - Jupyter Notebook used for processing the text dataset into numerical values with NLP
- Part3A_ML.ipynb - include Logistic Regression, Random Forest, and xgboost. This notebook is mainly to show previous workflow and the process of multiple iterations.
- Part3B_ML_v1.ipynb - Machine Learning with final approach using Random Forest
- Part3B_ML_v2.ipynb - Machine Learning with final approach using Logistic Regression and XGBoost
