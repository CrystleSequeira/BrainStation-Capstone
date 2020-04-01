## Use of NLP and supervised learning to predict wine scores

Original dataset is taken from [Kaggle](https://www.kaggle.com/zynicide/wine-reviews)

This is my final capstone project for the [BrainStation](https://brainstation.io/) Data Science Diploma Program. I decided to work with this dataset because the dataset contains over 100k rows and this is a text heavy dataset which is something I wanted to gain experience in. You can utilize this dataset in many different ways. My first approach to working with this dataset was to create a supervised learning model to target wine points.

#### Problem Statement:
Predicting how a wine will perform and understand why that wine performs well can be beneficial for consumers and sellers of wine. For example, a winemaker might want to gain insights into why their pinot noir is rated higher than their chardonnay. As well, wine distributers might want to make profitable decisions like is it worth it to invest in an expensive wine and will this wine sell. To delve into these questions, I created a predictive model to target wine scores and analyze a dataset that includes the geography of the wine, price, description, variety, and vintage.

#### Description of the dataset:
- Datatframe exported as a csv with information about wine
- Data was originally scraped from the kaggle user on www.winemag.com
- 130k rows and 12 columns
- Column Names: 
  - country - The country from where the wine is made
  - description - wine description from reviewer
  - designation - The vineyard within the winery 
  - points - Wine rating which range between 80 - 100. A rating can range between 0 - 100, however winemag.com only posts reviews that scored 80 and above.
  - price - Cost of a bottle of wine
  - province - Province where the wine is made
  - region_1 - The region from where the wine is made
  - region_2 - A subregion from where the wine is made
  - taster_name - Name of the taster who reviewed the wine
  - taster_twitter_handle - Taster's twitter handle
  - title - Title of the wine
  - variety - variety or blend of the wine such as Pinot Noir or Merlot
  - winery - The name of thet winery where the wine is made
  
#### Methods:
1. Clean data
- Missing Data
- Remove Columns
- EDA
- Transform the dependent variable (Points) into two classifications

2. Feature Engineering
- Extract Vintage from the title of the wine

3. NLP
- One-Hot-Encoder
- TF-IDF Vectorizer

4. Machine Learning
- Logistic Regression
- Random Forest
- XGBoost
- Hyperparameter Optimization 
- Pipline/Gridsearch
- Model Evaluation

5. Figures: 
[Tableau Public](https://public.tableau.com/profile/aviel.stern#!/vizhome/WineReviewsData_15847279378710/Sheet6)
---------------------------------------------------------

#### Python Packages needed to install: 
- conda install -c anaconda joblib
- conda install -c anaconda nltk
- conda install -c conda-forge xgboost
- conda install -c conda-forge geopy (Note: Did not end up using this package, but if you want to try to extract Latitude and Longitude as Features, you can use this package)

#### Data Folder 
- dummy_train.csv: This csv file is the dummy variables for variety, country, province from the train dataset. This file is important for making sure that future datasets contain the same features as the train dataset.
- train_clean.csv: Train dataset where missing values were removed, and non-essential columns were dropped.
- test_clean.csv: Test dataset where missing values were removed, and non-essential columns were dropped.
- model_train.csv: Train dataset that is ready for fitting a model
- model_test.csv: Test dataset that is ready for fitting a model

#### Machine Learning Model:
logreg_ml.pkl (Best performing model - Logistic Regression)

#### Notebook Folder:
- Part1_Clean_Wine_Reviews.ipynb - Jupyter Notebook used for cleaning the dataset which includes Missing Values, Drop Columns, and Feature Engineering
- Part2_NLP_Wine_Reviews.ipynb - Jupyter Notebook used for processing the text dataset into numerical values with NLP and transform wine scores into a two classification.
- Part3A_ML.ipynb - include Logistic Regression, Random Forest, and xgboost. This notebook is mainly to show previous workflow and the process of multiple iterations. This workbook is not to be used for future machine learning models to predict scores.
- Part3B_ML_v1.ipynb - Machine Learning with final approach using Random Forest
- Part3B_ML_v2.ipynb - Machine Learning with final approach using Logistic Regression and XGBoost
