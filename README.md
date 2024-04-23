# Ride Request Demand Forecasting

## Project Overview
### Business Problem
Ola Bikes are facing losses and stiff competition due to their inability to fulfill ride requests efficiently. The challenge is to predict the demand for rides in a specific region and future time window to allocate drivers intelligently and meet user requests effectively.

### Goal
The goal is to forecast ride requests (demand) for a particular latitude and longitude within a requested future time window.

## Data Description
The raw data contains unique user IDs, ride request timestamps (IST), pickup and drop locations latitude and longitude.

### Data Fields
1. `number`: Unique user ID
2. `ts`: Ride request DateTime (IST)
3. `pick_lat`: Pickup latitude
4. `pick_lng`: Pickup longitude
5. `drop_lat`: Drop latitude
6. `drop_lng`: Drop longitude

### Defining a Good Ride Request
1. Count only one ride request per user within 1 hour from the last booking.
2. Consider only one ride request within 8 minutes from the last booking.
3. Exclude ride requests with a geodesic distance less than 50 meters.
4. Exclude ride requests with pickup or drop locations outside India bounding box.
5. Exclude ride requests outside Karnataka bounding box with pickup and drop geodesic distance > 500 kms.

## Predict Task to Test Model
Ola provided filtered ride requests data for 2021-03-26 and requested initial hours rides request demand forecast for 2021-03-27 to test the prediction pipeline.

## Key Learning Objectives
- Understand multi-step time series forecasting concepts.
- Perform data exploration and cleaning.
- Implement Geospatial feature engineering and Mini-Batch K-Means clustering.
- Analyze correlation and lead-lag relationships.
- Evaluate models using Root Mean Square Error (RMSE).
- Implement machine learning algorithms (Linear Regression, Random Forest, XGBoost) for multi-step time series forecasting.

This project provides hands-on experience in solving real-world forecasting problems and implementing machine learning algorithms for demand forecasting in the transportation sector.

## Tech Stack
- joblib==1.0.1
- pandas==1.2.4
- numpy==1.20.2
- gpxpy==1.4.2
- geopy==2.1.0
- xgboost==1.4.1
- ML_Pipeline==0.02
- scikit_learn==0.24.2
