# Predicting Electric Vehicle Base MSRP Using Supervised Regression


## **Project Overview**
The transportation sector is rapidly evolving with the growing adoption of Electric Vehicles (EVs). Accurate prediction of EV prices helps manufacturers optimize pricing strategies, policymakers design incentives, and consumers make informed choices.

This project develops supervised regression models to predict the Base MSRP (Manufacturer’s Suggested Retail Price) of electric vehicles based on their features such as battery capacity, range, model year, and other specifications.

## **Dataset**
Source: U.S. Government Open Data (https://catalog.data.gov/dataset/electric-vehicle-population-data)

Description: The dataset contains EV models along with their specifications and corresponding Base MSRP values.

## **Key Features** :

Battery Capacity

Range

Model Year

Vehicle Type

Other technical specs

## **Problem Statement**
Predict the Base MSRP of electric vehicles using regression models, enabling insights into factors affecting pricing and improving price estimation accuracy.

## **Methodology**

#### ➤ Data Preprocessing

Handling missing values

Encoding categorical variables

Feature selection

Feature Scaling

StandardScaler to normalize numerical features

#### ➤ Model Implementation
Trained and evaluated multiple regression algorithms:

Linear Regression

Decision Tree Regressor

Random Forest Regressor

Gradient Boosting Regressor

Support Vector Regressor

#### ➤ Model Evaluation
Used performance metrics including:

R² Score

Mean Squared Error (MSE)

Mean Absolute Error (MAE)

Root Mean Squared Error (RMSE)

#### ➤ Hyperparameter Tuning

Performed Grid Search to optimize model parameters, improving prediction accuracy.

## **Conclusion**

After extensive preprocessing, model training, and tuning:

-  **Random Forest Regressor** delivered the best performance  
-  Demonstrated high accuracy in predicting EV prices  
-  Emphasized the importance of feature engineering and tuning  

Despite challenges like **zero-inflation in the target variable** and **high computational costs**, the model achieved reliable results and forms a strong foundation for future improvements.



## Limitations
- Large dataset posed memory and processing constraints  
- Target variable had zero-inflation and skewness  
- Model requires high compute power, limiting real-time use  
- May miss complex interactions due to limited model complexity  

## Future Scope and Impact
###  Practical Applications

- **Manufacturers**: Use model insights to strategize competitive EV pricing  
- **Policymakers**: Assess the impact of incentives on EV adoption  
- **Consumers**: Get price estimates aligned with features and budget  
- **Climate Impact**: Support sustainable and green transportation planning  

###  Potential Enhancements

- SHAP, LIME for **Model Explainability**  
- **Ensemble Learning**: Boosting, Bagging, Stacking  
- **Transfer Learning** using deep models  
- **Geospatial & Time-Series Analysis**  
- **Causal Inference** to understand deeper patterns  
- **Domain Adaptation** for other markets/regions  
- **Uncertainty Quantification** to assess model confidence  
- **Real-Time Deployment** via Flask/Streamlit APIs 
