This project builds a Machine Learning model to predict housing prices using the California Housing dataset.
It demonstrates a complete end-to-end machine learning pipeline including data preprocessing, stratified sampling, model training, and prediction.

📌 Project Overview
The main goal of this project is to predict the median house value based on different housing features such as:

Median income
Total rooms
Total bedrooms
Population
Households
Housing location
Ocean proximity
This project uses Random Forest Regressor along with a professional Scikit-Learn pipeline for preprocessing and prediction.

⚙️ Technologies Used
Python
Pandas
NumPy
Scikit-learn
Joblib
📊 Machine Learning Workflow
1. Data Loading
The California housing dataset is loaded using Pandas.

2. Stratified Sampling
The dataset is split using StratifiedShuffleSplit based on income_cat so that the train and test sets maintain a similar income distribution.

3. Data Preprocessing Pipeline
The project creates two pipelines:

Numerical Pipeline
Missing value handling using SimpleImputer(strategy="median")
Feature scaling using StandardScaler
Categorical Pipeline
Categorical feature transformation using OneHotEncoder(handle_unknown="ignore")
These two pipelines are combined using ColumnTransformer.

4. Model Training
A RandomForestRegressor model is trained on the prepared housing data.

5. Model Saving
The trained model and pipeline are saved using Joblib so they can be reused later without retraining.

Saved files:

model.pkl
pipline.pkl
6. Inference
If the saved model already exists, the program:

Loads the trained model
Loads the preprocessing pipeline
Reads input data from input.csv
Applies preprocessing
Predicts housing prices
Saves results in output.csv
