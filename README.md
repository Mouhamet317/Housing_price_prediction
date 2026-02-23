# Housing_price_prediction
Project Overview:
-------------
This project builds a high-performance regression model to predict California median house prices using structured tabular data.

The objective was not just to train a model, but to:

Apply meaningful feature engineering

Compare baseline and ensemble models

Evaluate generalization using cross-validation

Analyze model behavior and stability


Dataset: California Housing (from sklearn.datasets)
-----------
Target variable: Median House Value
-----------
Original features: 8 numerical socio-economic and geographic variables
-------------
Methodology
--------------------------------------------------------------------
1️-Baseline Model
-----------
Linear Regression
------------
R² ≈ 0.57

2️-Tree-Based Model
-------------------------
Random Forest
-----------------
R² ≈ 0.80

3️-Feature Engineering
-----------------------------
New features created:

Income per Room = MedInc / AveRooms

Rooms per Household = AveRooms / AveOccup

Regional Clusters using KMeans on latitude/longitude

These features improved spatial and economic signal extraction.

4-Final Model — XGBoost Regressor
----------------------------------
Gradient Boosting

200 estimators

Tuned learning rate

5-Fold Cross Validation
-----------------------
Results
---------------------------------------------------
Train/Test Split
Metric	Score
MAE	0.294
RMSE	0.455
R²	0.842
5-Fold Cross Validation

Mean R²: 0.844

Std R²: 0.006

Low standard deviation confirms strong generalization and model stability.

Model Insights:
--------------------------------------
Median Income remains the strongest predictor.

Engineered spatial clusters improved predictive power.

Gradient boosting significantly outperformed linear models.

Learning rate sensitivity analysis showed performance degradation at high learning rates.

Key Takeaways
----------------------------------
Feature engineering significantly impacts tabular model performance.

Ensemble methods capture non-linear interactions effectively.

Cross-validation is essential for reliable performance estimation.

Small hyperparameter adjustments can meaningfully improve generalization.

Skills Demonstrated
----------------------------------------
Exploratory Data Analysis

Feature Engineering

Gradient Boosting (XGBoost)

Cross-Validation

Hyperparameter Sensitivity Analysis

Model Evaluation & Interpretation

Data Visualization

Future Improvements
---------------------------
Hyperparameter tuning with GridSearchCV

LightGBM / CatBoost comparison

SHAP for model explainability

Incorporating external socio-economic datasets

Tech Stack
--------------------------
Python

Scikit-learn

XGBoost

Pandas

NumPy

Matplotlib

Author: Mouhamadou SOW
------------------
