This project builds a Machine Learning model to predict housing prices using the California Housing dataset.
It demonstrates a complete end-to-end machine learning pipeline including data preprocessing, stratified sampling, model training, and prediction.

Project Overview:

The main goal of this project is to predict the median house value based on different housing features such as:
1. Median income
2. Total rooms
3. Total bedrooms
4. Population
5. Households
6. Housing location
7. Ocean proximity
This project uses Random Forest Regressor along with a professional Scikit-Learn pipeline for preprocessing and prediction.

Technologies Used:

1. Python
2. Pandas
3. NumPy
4. Scikit-learn

Machine Learning Workflow:

1. Data Loading
The California housing dataset is loaded using Pandas.

2. Stratified Sampling
The dataset is split using StratifiedShuffleSplit based on income_cat so that the train and test sets maintain a similar income distribution.

3. Data Preprocessing Pipeline
The project creates two pipelines:
A. Numerical Pipeline- Missing value handling using SimpleImputer(strategy="median") and Feature scaling using StandardScaler
B. Categorical Pipeline- Categorical feature transformation using OneHotEncoder(handle_unknown="ignore")

These two pipelines are combined using ColumnTransformer.

4. Model Training
A RandomForestRegressor model is trained on the prepared housing data.

5. Model Saving
The trained model and pipeline are saved using Joblib so they can be reused later without retraining.
