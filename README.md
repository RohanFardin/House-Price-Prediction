# House-Price-Prediction
House Price Prediction Using Random Forest: A Machine Learning Repository

## Introduction  
House price prediction is a common machine learning task. In this project, we use the Random Forest regression algorithm to predict house prices based on key features from a dataset. The goal is to create a reliable model that can assist in property valuation.

---

## Dataset  
The dataset includes various features such as:  
- Property details (e.g., `OverallQual`, `GrLivArea`, `TotalBsmtSF`)  
- Location-specific information (e.g., `Neighborhood`)  
- Additional features engineered during preprocessing  

The target variable is `SalePrice`.  

---

## Features  
Below are the features used for prediction:  
- `OverallQual`: Overall material and finish quality  
- `OverallCond`: Overall condition rating  
- `YearBuilt`: Original construction date  
- `YearRemodAdd`: Remodel date  
- `GrLivArea`: Above ground living area in square feet  
- `TotalBsmtSF`: Total square footage of the basement  
- `Neighborhood`: Location-based neighborhood  
- `LotArea`: Lot size in square feet  
- `FullBath`: Full bathrooms above grade  
- `BedroomAbvGr`: Number of bedrooms above grade  
- `GarageCars`: Size of the garage (in cars)  
- `GarageArea`: Garage size in square feet  
- `ExterQual`: Exterior quality  
- `KitchenQual`: Kitchen quality  
- `SaleCondition`: Condition of sale  
- `HouseAge`: Age of the house at the time of sale  
- `TotalBath`: Total bathrooms, including basement  
- `TotalPorchSF`: Combined porch areas  

---

## Preprocessing Steps  
The following steps were performed to prepare the dataset:  
1. **Feature Engineering**:  
   - Created new features such as `HouseAge`, `RemodelAge`, `TotalBath`, and `TotalPorchSF`.  

2. **Handling Missing Values**:  
   - Categorical features were filled with the mode or a default category (e.g., "Unknown" or "None").  
   - Numerical features were filled with median values or default values such as `0` for missing data (e.g., no garage or no porch).  

3. **Encoding Categorical Features**:  
   - Used `LabelEncoder` to transform categorical features into numeric representations.  

4. **Scaling Numerical Features**:  
   - Applied `StandardScaler` to normalize numerical features for consistent scaling.  

5. **Neighborhood Median Mapping**:  
   - Mapped `Neighborhood` to its median house price as a new feature.  

---

## Model Training  
A Random Forest Regressor was used for predicting house prices. Below are the key steps:  
1. Split the dataset into training and testing sets using `train_test_split`.  
2. Trained the model using the `RandomForestRegressor` with 100 estimators and a random state for reproducibility.  

---

## Performance Evaluation  
The performance of the model was evaluated using:  
- **Mean Absolute Error (MAE)**: Measures the average magnitude of errors in predictions.  
