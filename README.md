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

## Features Used

The final model uses:

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

Categorical variables are encoded using One-Hot Encoding, while numerical variables are imputed and standardized.

## Results

The final model achieved approximately:

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