# 🚗 In-Vehicle Coupon Recommendation System
Overview

This project develops an end-to-end Machine Learning classification model to predict whether a driver will accept an in-vehicle coupon based on contextual, demographic, and behavioral information.

The objective is to help advertisers deliver coupons to users who are more likely to redeem them, thereby improving coupon acceptance rates and reducing ineffective marketing campaigns.

## Business Problem

Traditional coupon campaigns often send offers to users without considering their current driving context or preferences.

This project predicts:

  **Will the driver accept the coupon?**

using contextual driving information and user attributes.

The prediction can help businesses:

- Improve coupon acceptance
- Personalize marketing campaigns
- Increase customer engagement
- Reduce unnecessary promotional costs

## Dataset
- Source: UCI / Amazon Mechanical Turk Survey
- Records: ~12,000
- Features: 24
- Target:
     **Accept Coupon (Yes/No)**

Example features include:

- Destination
- Passenger
- Weather
- Temperature
- Coupon Type
- Expiration
- Income
- Occupation
- Education
- Driving Distance
- Direction
- Restaurant Visits
- Coffee House Visits
- Bar Visits
  
## Project Workflow
**1. Business Understanding**
- Defined business objective
- Identified stakeholders
- Framed as Binary Classification
  
**2. Exploratory Data Analysis**

Performed EDA to identify behavioural patterns.

Key findings:

- Cheap restaurant coupons showed the highest acceptance.
- Carry-away coupons performed well.
- Bar coupons had the lowest acceptance.
- One-day coupons were accepted more often than two-hour coupons.
- Passenger type and destination influenced acceptance.
  
**3. Data Cleaning & Preprocessing**
- Removed duplicate records
- Dropped Car column (~99% missing)
- Imputed missing values using mode
- One-hot encoded categorical variables
- Stratified train-test split
- Prepared data for ML models
  
**4. Machine Learning Models**

Models evaluated:

- Logistic Regression
- Decision Tree
- Random Forest
  
**5. Hyperparameter Tuning**

Random Forest was optimized using

- RandomizedSearchCV
- 5-Fold Cross Validation

Parameters tuned included:

- n_estimators
- max_depth
- min_samples_split
- min_samples_leaf
- max_features
- bootstrap
  
## Model Performance
- **Model		 Accuracy**
- Logistic Regression	~68%
- Decision Tree	~70%
- Random Forest	~74%
- Tuned Random Forest	~75%

**Final Model:**

- Accuracy: ~75%
- Recall: ~83%
  
## Key Insights

The most influential factors affecting coupon acceptance were:

- Coupon Type
- Coupon Expiration
- Destination
- Passenger
- Time of Day

The project demonstrates that contextual information plays a significant role in predicting customer behavior.

## Tech Stack
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Random Forest
- Logistic Regression
- Decision Tree
  

## Future Improvements
- XGBoost
- LightGBM
- SHAP Explainability
- Feature Engineering
- Model Deployment using Flask/FastAPI
- Streamlit Dashboard
  
## Results

The tuned Random Forest successfully predicted coupon acceptance with approximately 75% test accuracy while achieving 83% recall, making it a reliable model for targeted coupon recommendation.

## Author

**Roshan J Mathew**
