# Predicting Electric Vehicle Base MSRP Using Supervised Regression

##  Problem Statement  
The goal of this project is to develop a **regression model** that accurately predicts the **Base MSRP (Manufacturer’s Suggested Retail Price)** of electric vehicles (EVs) using their specifications.

Understanding how factors like **battery capacity**, **range**, and **model year** affect EV pricing is crucial for:  
- **Manufacturers** to optimize pricing strategies  
- **Policymakers** to evaluate incentive programs  
- **Consumers** to make informed purchase decisions

---

##  Dataset Overview  
- **Source**: [Electric Vehicle Population Data – Data.gov](https://catalog.data.gov/dataset/electric-vehicle-population-data)  
- **Type**: Public government dataset  
- **Format**: CSV  
- **Size**: 223,995 rows × 17 columns  

###  Key Features  
- `Battery Capacity (kWh)`  
- `All-Electric Range (miles)`  
- `Model Year`  
- `Vehicle Type`  
- `Base MSRP (Target)`  
- Additional categorical and technical specs  

---

##  Project Type  
- **Learning Type**: Supervised Learning  
- **Modeling Task**: Regression  
- **Target Variable**: `Base MSRP`

---

##  Methodology

### 1. Data Preprocessing  
- **Missing Values**  
  - Numerical: Imputed with **mean**  
  - Categorical: Imputed with **mode**  
- **Outlier Detection**: Removed using **IQR method**  
- **Skewness Handling**: Addressed using transformation methods  
- **Encoding**: Used `LabelEncoder` for categorical variables  
- **Feature Scaling**: Standardized using `StandardScaler`  
- **Feature Selection**: Selected relevant features based on correlation and domain relevance

---

### 2. Model Implementation  
| Model                      | Algorithm Used             |
|---------------------------|----------------------------|
| Linear Regression         | `LinearRegression()`       |
| Decision Tree Regressor   | `DecisionTreeRegressor()`  |
| Random Forest Regressor   | `RandomForestRegressor()`  |
| Gradient Boosting Regressor | `GradientBoostingRegressor()` |
| Support Vector Regressor  | `SVR()`                    |
| MLP Regressor             | `MLPRegressor()`           |

---

### 3. Model Evaluation Metrics  
- **R² Score**  
- **Mean Squared Error (MSE)**  
- **Mean Absolute Error (MAE)**  
- **Root Mean Squared Error (RMSE)**  

###  Best Model: Random Forest Regressor 

---

### 4. Hyperparameter Tuning  
- **Technique**: `GridSearchCV`  
- **Objective**: Improve performance by tuning `n_estimators`, `max_depth`, and other parameters  
- **Result**: Enhanced accuracy and generalization

---

### 5. Pipeline Creation  
To ensure automation and scalability, a pipeline was created:  
1. Preprocessing  
2. Feature Scaling  
3. Model Training  
4. Evaluation

---

###  Model Saving  
- Trained model saved using `Pickle` or `Joblib`  
- Enables **future deployment or inference**

---

##  Key Insights  
- Tree-based ensemble methods outperform others for this dataset  
- Feature engineering and preprocessing critically impact performance  
- High `R²` value indicates strong explanatory power

---

##  Visual Evaluation  
- **Residual Plots**: Checked for randomness of errors  
- **Actual vs Predicted**: Confirmed tight fit  
- **Feature Importance**: Identified influential features like battery capacity and range

---

##  Limitations  
- **High memory usage** for full dataset  
- **Skewed target variable** with zero-inflation  
- **Long training time** for large models like Random Forest & MLP  
- Limited handling of **feature interactions** in simpler models

---

##  Future Scope & Real-World Impact  

###  Applications  
- **Manufacturers**: Use model insights for price optimization  
- **Policymakers**: Evaluate EV incentive program effectiveness  
- **Consumers**: Get realistic price expectations  
- **Sustainability**: Supports EV adoption & climate action goals  

###  Potential Enhancements  
-  **Model Explainability**: SHAP, LIME  
-  **Ensemble Learning**: Boosting, Bagging, Stacking  
-  **Transfer Learning** & DNNs  
-  **Geospatial & Time-Series** features  
-  **Real-time Deployment**: Flask, Streamlit  
-  **Uncertainty Quantification**




