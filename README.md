# Predicting Electric Vehicle Base MSRP Using Supervised Regression

##  Project Overview

The transportation sector is rapidly evolving with the growing adoption of Electric Vehicles (EVs). Accurate prediction of EV prices helps manufacturers optimize pricing strategies, policymakers design incentives, and consumers make informed choices.

This project develops supervised regression models to predict the Base MSRP (Manufacturer’s Suggested Retail Price) of electric vehicles based on their features such as battery capacity, range, model year, and other specifications.

-  Helping **manufacturers** optimize pricing strategies  
-  Enabling **policymakers** to design effective incentive programs  
-  Assisting **consumers** in making informed purchase decisions

This project builds supervised regression models to predict the **Base MSRP** (Manufacturer’s Suggested Retail Price) of EVs based on specifications like battery capacity, range, model year, and more.

---

##  Dataset

- **Source:** [U.S. Government Open Data](https://catalog.data.gov/dataset/electric-vehicle-population-data)  
- **Description:** Contains detailed records on electric vehicles registered in the U.S.  
- **Records:** 223,995 rows and 17 columns
  
##  **Key Features:**
  - Battery Capacity (kWh)
  - All-Electric Range (miles)
  - Vehicle Model Year
  - Vehicle Type
  - Base MSRP (target variable)
  - Technical and categorical specs

---

##  Problem Statement

> **Goal:** Predict the Base MSRP of electric vehicles using supervised learning techniques to improve pricing strategy, policy planning, and consumer decision-making.

---

##  Methodology

###  Data Preprocessing

- **Missing Values:**
  - Numerical: Imputed with mean  
  - Categorical: Imputed with mode  
- **Encoding:** Used `LabelEncoder` for categorical features  
- **Outlier Removal:** Applied IQR method  
- **Skewness Handling:** Used transformations to reduce skew  
- **Scaling:** Normalized numerical features using `StandardScaler`  
- **Feature Selection:** Chose relevant columns for accurate prediction

---

###  Model Implementation

The following regression models were implemented and evaluated:

| Model                      | Algorithm Used             |
|---------------------------|----------------------------|
| Linear Regression         | `LinearRegression()`       |
| Decision Tree Regressor   | `DecisionTreeRegressor()`  |
| Random Forest Regressor   | `RandomForestRegressor()`  |
| Gradient Boosting Regressor | `GradientBoostingRegressor()` |
| Support Vector Regressor  | `SVR()`                    |
| MLP Regressor             | `MLPRegressor()`           |

---

###  Model Evaluation

Used the following metrics to compare models:

- R² Score  
- Mean Squared Error (MSE)  
- Mean Absolute Error (MAE)  
- Root Mean Squared Error (RMSE)

 **Best Model:** `Random Forest Regressor`

---

###  Hyperparameter Tuning

- **Method:** `GridSearchCV`  
- **Goal:** Optimize hyperparameters of Random Forest for improved performance  
- **Result:** Increased model accuracy with tuned parameters

---

###  Pipeline Creation

To ensure efficiency and reproducibility, a pipeline was created including:

1. Data Preprocessing  
2. Feature Scaling  
3. Model Training (Random Forest Regressor)

---

###  Model Saving

- The final trained model was saved using `Pickle`/`Joblib` for future inference or deployment.

---

##  Conclusion

- Random Forest Regressor provided the best accuracy among all models.  
- Proper data cleaning, feature engineering, and hyperparameter tuning were essential.  
- The model can assist manufacturers, policymakers, and consumers with pricing predictions.

---

##  Limitations

- Large dataset required significant memory and processing time  
- Target variable (Base MSRP) had skewness and zero-inflation  
- High computational cost limits real-time usage  
- Potential underfitting of complex feature interactions

---

##  Future Scope & Real-World Impact

###  Practical Applications

- **Manufacturers:** Price optimization based on feature patterns  
- **Policymakers:** Assess incentive effectiveness on EV adoption  
- **Consumers:** Get price estimates based on specs  
- **Climate Strategy:** Support green and sustainable planning

###  Potential Enhancements

- Model Explainability using **SHAP** or **LIME**  
- Ensemble learning: Boosting, Bagging, and Stacking  
- **Transfer Learning** and deep neural models  
- **Geospatial & Time-Series** feature integration  
- **Causal Inference** for deeper pricing logic  
- Real-time deployment using **Flask** or **Streamlit** APIs  
- **Uncertainty Quantification** for prediction confidence

---



