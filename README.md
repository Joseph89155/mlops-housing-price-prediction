# 🏠 MLOps: Housing Price Prediction using the California Housing Dataset

## 📌 Project Overview

This project showcases an end-to-end machine learning workflow for predicting median housing prices in California. Using the 1990 California census data, we train a regression model that learns patterns from demographic and geographic attributes to predict house values.

Built with MLOps principles in mind, the project includes preprocessing, pipeline construction, hyperparameter tuning, model evaluation, and deployment through a simple Flask API.

---

## 🎯 Objectives

- Load and prepare the California Housing dataset
- Apply preprocessing using `ColumnTransformer` and `StandardScaler`
- Build a pipeline with `KNeighborsRegressor`
- Tune hyperparameters using `GridSearchCV` with 5-fold cross-validation
- Evaluate model performance using **R² score**
- Save the trained pipeline with `joblib`
- Deploy the model using a minimal Flask API (`/predict` endpoint)

---

## 🗂️ Dataset

- **Source**: `fetch_california_housing()` from Scikit-learn
- **Target**: Median house value (`MedHouseVal`) in $100,000s
- **Features**:
  - `MedInc`: Median income
  - `HouseAge`: Median house age
  - `AveRooms`: Average rooms per household
  - `AveBedrms`: Average bedrooms per household
  - `Population`: Block group population
  - `AveOccup`: Average household size
  - `Latitude`: Latitude
  - `Longitude`: Longitude

---

## 🧠 Model & Tools

- **Model**: `KNeighborsRegressor` from Scikit-learn
- **Preprocessing**: `StandardScaler` inside `ColumnTransformer`
- **Pipeline**: Scikit-learn’s `Pipeline` API
- **Tuning**: `GridSearchCV` over:
  - `n_neighbors`: [3, 5, 7, 9]
  - `weights`: ['uniform', 'distance']
  - `p`: [1, 2]
- **Evaluation Metric**: R² Score
- **Deployment**: Flask-based API with a `/predict` endpoint

---

## ✅ Results

- **Best R² Score on Test Set**: `0.7221`
- **Best Parameters**: Automatically selected via GridSearchCV
- **Model Saved As**: `knn_housing_model.pkl`

---

🌍 Real-World Applications
 - Real estate price estimation

 - Mortgage risk modeling

 - Urban and regional planning

 - Real-time valuation tools for housing platforms

---

🧑‍💻 Author

Name: Joseph Maina

GitHub: @Joseph89155

---

📄 License
This project is licensed under the MIT License.

---
