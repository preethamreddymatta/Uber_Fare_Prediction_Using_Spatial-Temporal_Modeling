# Uber_Fare_Prediction_Using_Spatial-Temporal_Modeling
Uber Fare Prediction Using Machine Learning
# Overview

Ride-sharing pricing is influenced by multiple factors such as trip distance, time of day, weekday patterns, and location dynamics. However, raw trip data does not explicitly reveal how these variables impact fare pricing.

This project builds a machine learning pipeline to predict Uber ride fares using 190,000+ trip records. By combining exploratory data analysis, feature engineering, and regression modeling, the goal is to improve prediction accuracy and minimize error (RMSE).

 ## Problem Statement

How can we accurately predict Uber ride fares using trip-level data?

This project focuses on:

Estimating fare amounts using historical trip data
Capturing spatial and temporal patterns through feature engineering
Comparing multiple regression models to identify the best-performing approach
# Dataset
Size: 190K+ Uber trip records
Key Features:
Pickup & drop-off coordinates (latitude, longitude)
Fare amount
Timestamp (date & time of trip)
Passenger count
# Project Pipeline
## 1.  Data Cleaning
Removed invalid fares (negative/zero values)
Filtered out zero-distance trips
Handled extreme outliers to stabilize model training
## 2.  Feature Engineering
Geospatial Features
Haversine Distance (primary distance metric)
Optional:
Manhattan distance
Bearing/direction between locations
Temporal Features
Hour of day
Day of week
Rush-hour indicators
Seasonal patterns
## 3.  Exploratory Data Analysis (EDA)
Identified trip distance as the strongest predictor
Observed temporal trends (peak hours, weekday patterns)
Visualized fare distributions and outliers
## 4.  Model Development
Models Implemented:
Linear Regression
Random Forest Regressor
XGBoost Regressor
Training Strategy:
Train/test split
Cross-validation
## 5.  Hyperparameter Tuning
Used GridSearchCV to optimize model parameters
Focused on improving:
RMSE (Root Mean Squared Error)
R² (Coefficient of Determination)
## 6.  Model Evaluation
Model	RMSE	R²
Linear Regression	Baseline	Moderate
Random Forest	4.32	~0.79
XGBoost	Competitive	High

# Best Model: Random Forest (after tuning)

RMSE improved from 5.08 → 4.32 (~15% improvement)
Achieved R² ≈ 0.79
## 7.  Model Interpretability
Feature importance analysis (tree-based models)
Distance identified as the dominant feature
Temporal variables added incremental predictive power
# Key Insights
Trip distance is the primary driver of fare
Rush-hour and weekday patterns influence pricing
Feature engineering significantly improves model performance
Ensemble models outperform linear models for this task
