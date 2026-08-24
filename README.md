# NYC Taxi Fare Prediction

A machine learning project to predict NYC Yellow Taxi trip fares using trip, location, payment, and time-based features.

## Project Overview

This project analyzes NYC Yellow Taxi trip data and develops a regression model to predict the fare amount of a trip.

The project covers:

- Data exploration and cleaning
- Outlier and anomaly detection
- Feature engineering
- Exploratory data analysis
- Regression modeling
- Model evaluation
- Residual and error analysis

## Dataset

The project uses NYC Yellow Taxi trip data for January 2025.

The original dataset contains approximately 3.48 million trips.

The dataset includes information such as:

- Trip distance
- Trip duration
- Passenger count
- Rate code
- Pickup and drop-off locations
- Payment type
- Pickup time
- Fare amount

The raw dataset is not included in this repository because of its size.

## Data Cleaning

The dataset was cleaned by identifying and removing invalid or anomalous records, including:

- Negative fare amounts
- Invalid trip distances
- Invalid trip durations
- Unrealistic trip speeds
- Extreme fare outliers

The cleaned dataset was then used for feature engineering and model development.

## Features Used

The final model uses 14 features:

- `trip_distance`
- `trip_duration`
- `avg_speed_mph`
- `passenger_count`
- `RatecodeID`
- `PULocationID`
- `DOLocationID`
- `payment_type`
- `pickup_hour`
- `pickup_day`
- `pickup_day_of_month`
- `pickup_month`
- `is_weekend`
- `is_rush_hour`

## Model

The first predictive model is a Linear Regression model with preprocessing for numerical and categorical features.

Numerical features are:

- Imputed using median values where necessary
- Standardized using `StandardScaler`

Categorical features are:

- Imputed using the most frequent value
- Encoded using `OneHotEncoder`

The model is evaluated on a held-out test set.

## Results

The final Linear Regression model achieved approximately:

| Metric | Score |
|---|---:|
| MAE | 1.66 |
| RMSE | 3.95 |
| R² | 0.939 |

The model explains approximately 94% of the variance in fare amount on the test set.

## Project Structure

```text
nyc-taxi-fare-prediction/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── 01_exploration.ipynb
│   └── 02_linear_regression.ipynb
│
├── results/
│
├── src/
│
├── .gitignore
├── README.md
└── requirements.txt
