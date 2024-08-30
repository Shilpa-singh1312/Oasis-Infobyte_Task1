# Oasis-Infobyte_Task1
Car Price Prediction with Machine Learning 
Overview
This project aims to predict the selling price of cars using machine learning models. The price of a car is influenced by various factors such as the brand's goodwill, car features, horsepower, and mileage. In this project, we use Linear Regression and Ridge Regression to model and predict car prices. This project provides an excellent opportunity to learn how to train and evaluate car price prediction models.
Table of Contents
Features
Data Preprocessing
Model Training
Model Evaluation
Prediction
Code Analysis
Summary and Analysis
How to Run
Requirements
License
Features
Year: The year of manufacture of the car.
Driven_kms: The number of kilometers the car has been driven.
Present_Price: The current price of the car.
Fuel_Type: Type of fuel used (e.g., Petrol, Diesel).
Selling_type: Type of selling (e.g., Dealer, Individual).
Transmission: Transmission type (e.g., Manual, Automatic).
Owner: Number of previous owners.
Data Preprocessing
Load Data: The dataset is loaded from car data.csv.
Label Encoding: Categorical variables (Fuel_Type, Selling_type, Transmission) are converted to numerical values using LabelEncoder.
Feature Scaling: Features are scaled using StandardScaler to ensure comparability and improve model performance.
Train-Test Split: Data is split into training and testing sets with an 80-20 split.
Model Training
Linear Regression: A linear regression model is trained on the scaled training data.
Ridge Regression: A ridge regression model (with alpha = 1.0) is trained on the scaled training data.
Model Evaluation
Linear Regression:

Mean Squared Error (MSE): 6.68
R-squared (R²): 0.74
Ridge Regression:

Mean Squared Error (MSE): 6.67
R-squared (R²): 0.74
Both models show similar performance, explaining approximately 74% of the variance in car prices.

Prediction
Using the trained models, predictions are made for a new car with the following features:

Year: 2024

Driven_kms: 20,000

Present_Price: 20,000

Fuel_Type: Petrol

Selling_type: Dealer

Transmission: Manual

Owner: 0

Predicted Selling Price (Linear Regression): $8,802.59

Predicted Selling Price (Ridge Regression): $8,747.15

Code Analysis
Original Feature Ranges:

Year: 2003 - 2018
Driven_kms: 500 - 500,000
Present_Price: 0.32 - 92.6
Scaled Feature Ranges:

Year: -3.71 to 1.16
Driven_kms: -1.21 to 6.34
Present_Price: -0.81 to 9.66
Scaling ensures feature comparability, leading to more effective modeling.

Summary and Analysis
Model Effectiveness: Both Linear and Ridge Regression models perform well, with an R² of 0.85, indicating a strong fit to the data. The marginal difference in MSE suggests regularization has a minimal impact on performance.
Feature Scaling: Proper scaling of features ensures that all variables contribute equally, enhancing model stability and performance.
Predictions: Predictions are realistic and consistent with the dataset, demonstrating the models' reliability in estimating car prices.
How to Run
Ensure you have the required dependencies installed (see Requirements).
Place the dataset car data.csv in the project directory.
Run the script car_price_prediction.py to train the models and make predictions.
bash
python car_price_prediction.py
Requirements
Python 3.x
pandas
numpy
scikit-learn
You can install the required packages using pip:

bash
pip install pandas numpy scikit-learn
