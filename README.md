# House-pricing-using-ML-models-

🏡 House Price Prediction using Machine Learning
🔹 Objective

The goal of this project is to develop a machine learning model that can accurately predict the price of a house based on its physical attributes (like area, bedrooms, and bathrooms) and amenities (like air conditioning, basement, and furnishing type).
This helps real estate agencies and buyers make data-driven decisions in property evaluation.

🔹 Dataset Overview

The dataset used is Housing.csv, which contains 545 house records with features such as:

Numerical features: area, bedrooms, bathrooms, stories, parking

Categorical features: mainroad, guestroom, basement, hotwaterheating, airconditioning, prefarea, furnishingstatus

Target variable: price

Each record represents a unique house along with its characteristics and selling price.

🔹 Data Preprocessing

Handling Categorical Variables:

Binary categorical columns like yes/no were converted to 1/0.

Multi-category variables like furnishingstatus were encoded using One-Hot Encoding (via pd.get_dummies).

Missing Values:

The dataset contained no missing values, ensuring clean input for model training.

Feature Selection:

The independent features (X) include all columns except price.

The dependent feature (y) is the price column.

🔹 Model Training and Evaluation

Data Split:

Dataset was split into 80% training and 20% testing sets using train_test_split.

Models Implemented:

Linear Regression

Lasso Regression

Decision Tree Regressor

Performance Evaluation:

Used R² Score to measure how well the model explains variance in house prices.

Applied Cross-Validation (ShuffleSplit) to ensure model stability.

Performed Grid Search (GridSearchCV) to find the best hyperparameters for all models.

Results:

The Linear Regression model performed the best with an average R² score around 0.65–0.70, meaning it can explain approximately 65–70% of the price variation.

🔹 Model Deployment

The final model (Linear Regression) was trained on the entire dataset.

The trained model was saved as:

housing_price_model.pkl — serialized model file.

columns.json — stores feature names used for prediction.

A custom predict_price() function was developed to take house parameters (area, rooms, amenities, etc.) and return an estimated price.

Example predictions:

House 1 Price: 6041320.85
House 2 Price: 9274796.58
