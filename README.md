# KaggleX-Skill-Assessment
In this challenge by predicting the price of a used vehicle

---

## Car Price Prediction

This repository contains the code and data for predicting car prices using a linear regression model. The dataset includes various features of cars, such as brand, model, year, mileage, fuel type, engine size, transmission type, exterior color, interior color, accident history, and title status. The goal is to predict the price of cars based on these features.

## Data Description

The dataset consists of two CSV files:
- `train.csv`: Contains the training data with features and the target variable `price`.
- `test.csv`: Contains the test data with features for which we need to predict the `price`.

## Preprocessing

The preprocessing steps include:
1. **Loading the data**:
   - The training and test datasets are loaded using pandas.

2. **Handling missing values**:
   - Rows with missing values in the training set are dropped to ensure data quality.

3. **Separating features and target variable**:
   - Features (`X_train`) and the target variable (`y_train`) are separated from the training data.

4. **Defining numerical and categorical features**:
   - Numerical features: `model_year`, `milage`
   - Categorical features: `brand`, `model`, `fuel_type`, `transmission`, `ext_col`, `int_col`, `engine`, `accident`, `clean_title`

5. **Creating preprocessing pipelines**:
   - **Numerical data**:
     - Imputation using the median.
     - Scaling using `StandardScaler`.
   - **Categorical data**:
     - Imputation using the most frequent value.
     - One-hot encoding.

## Model Training

The model pipeline includes:
- **Preprocessing steps**:
  - Using `ColumnTransformer` to apply the preprocessing steps to numerical and categorical data.
- **Model**:
  - A `LinearRegression` model is used to predict car prices.

The pipeline ensures that preprocessing and modeling steps are combined and executed seamlessly.

## Prediction

- The trained model is used to predict the prices for the test dataset.
- The predictions are stored in a new column `predicted_price` in the test dataset.

## Submission

The submission file `sample_submission.csv` contains:
- `id`: The unique identifier for each car.
- `predicted_price`: The predicted price of the car.

## Files

- `train.csv`: Training data.
- `test.csv`: Test data.
- `predict_car_prices.py`: Script for training the model and making predictions.
- `sample_submission.csv`: The submission file with predicted prices.
