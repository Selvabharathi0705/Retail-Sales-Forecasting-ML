# Retail-Sales-Forecasting-ML
## Overview
This project focuses on forecasting Walmart sales using various machine learning and deep learning techniques. The dataset used for this analysis is sourced from the [Walmart Recruiting - Store Sales Forecasting Kaggle Competition.](https://www.kaggle.com/c/walmart-recruiting-store-sales-forecasting) The project employs techniques like data preprocessing, feature engineering, and model building to predict weekly sales.

## Datasets
- **train.csv:** Contains sales data with attributes such as Store, Dept, Date, Weekly_Sales, and IsHoliday.
- **stores.csv:** Provides information about Walmart stores including Store, Type, and Size.
- **features.csv:** Includes additional features like Temperature, Fuel_Price, Markdowns, CPI, Unemployment, and IsHoliday.

## Machine Learning Models
- Linear Regression Model
- Random Forest Regression Model
- K Neighbors Regression Model
- XGBoost Regression Model
- DeepLearning Neural Network

## Data Preprocessing
- **Handling Missing Values:** Filled missing values using the median of respective columns.
- **Merging Datasets:** Combined main dataset with store and feature datasets.
- **Data Transformation:** Converted Date column into datetime format and set it as the index.
- **Feature Engineering:** Extracted Year, Month, and Week from Date column.
- **Aggregated Weekly Sales:** Calculated statistics like max, min, mean, median, and standard deviation of weekly sales.
- **Outlier Detection:** Removed outliers using z-score and eliminated negative weekly sales.
- **One-Hot-Encoding:** Applied one-hot encoding to categorical columns.
- **Data Normalization:** Normalized numerical columns using MinMaxScaler.

## Model Performance
- **Linear Regression Model**
  - Accuracy: 92.28%  
  - Mean Absolute Error: 0.0300
  - Mean Squared Error: 0.00348
  - Root Mean Squared Error: 0.059035
  - Explained Variance Score: 0.9228079

- **Random Forest Regression Model**
  - Accuracy: 97.88%
  - Mean Absolute Error: 0.15538
  - Mean Squared Error: 0.0009544
  - Root Mean Squared Error: 0.0308949
  - Explained Variance Score: 0.97885932

- **K Neighbors Regression Model**
  - Accuracy: 92.733%
  - Mean Absolute Error: 0.031032
  - Mean Squared Error: 0.00328085
  - Root Mean Squared Error: 0.057278
  - Explained Variance Score: 0.9284879

- **XGBoost Regression Model**
  - Accuracy: 97.301%
  - Mean Absolute Error: 0.01980200
  - Mean Squared Error: 0.00121835
  - Root Mean Squared Error: 0.03490499
  - Explained Variance Score: 0.9730149924
  
- **DNN**
  - Accuracy: 97.19%
  - Mean Absolute Error: 0.05863234
  - Mean Squared Error: 0.005591697
  - Root Mean Squared Error: 0.07477765
  - Explained Variance Score: 0.9105808
  - Kernel Initializer - normal
  - Optimizer - adam
  - The input_dim parameter is set to the number of features in the training dataset, which is determined by accessing the second element of the tuple returned by X_train.shape, and the output layer consists of 64 dimensions with the ReLU activation function.
  - 1 hidden layer with 32 nodes
  - Output layer with 1 node
  - Batch Size - 5000
  - Epochs - 100
