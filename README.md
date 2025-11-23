# ARIMA Forecasting Project

## 1. Purpose
This project analyzes a website traffic time series and builds forecasting models using ARIMA techniques.
Both a manually configured ARIMA model and an automatically selected ARIMA model are trained and compared using standard accuracy metrics.

## 2. Execution Steps

### Step 1 — Load Libraries
Import all necessary Python libraries (pandas, numpy, matplotlib, statsmodels, sklearn, pmdarima).

### Step 2 — Load Dataset
Load the dataset from GitHub:
A publicly available time series dataset from "LianneWriting" containing anonymized website traffic.

### Step 3 — Exploratory Analysis
- Inspect dataset structure
- Plot the raw time series
- Apply log transformation to stabilize variance

### Step 4 — Preprocessing
- Split data into training and test sets
- Check stationarity using:
  - Time series plot
  - ACF/PACF plots
  - Augmented Dickey-Fuller (ADF) test
- Difference the series to achieve stationarity

### Step 5 — Determine ARIMA Parameters
Use ACF and PACF plots to guide selection of ARIMA parameters (p, d, q).

### Step 6 — Train Manual ARIMA Model
Fit an ARIMA(2,1,0) model using statsmodels.

### Step 7 — Train Auto ARIMA Model
Use pmdarima's auto_arima to automatically find the best ARIMA configuration (returned: ARIMA(5,1,0)).

### Step 8 — Forecasting
Generate predictions for the test set using both models.

### Step 9 — Model Evaluation
Evaluate and compare ARIMA(2,1,0) and Auto ARIMA using:
- Mean Absolute Error (MAE)
- Mean Absolute Percentage Error (MAPE)
- Root Mean Squared Error (RMSE)

### Step 10 — Visualization
Plot:
- Actual vs predicted values
- Forecasted values for both models

## 3. Dataset Information
- Source: https://github.com/liannewriting/YouTube-videos-public
- File: website_data.csv
- Description: Time series of website visits. Dates removed for privacy.
- License: No explicit license provided by the dataset creator.

## 4. Versions Used
- Python 3.10
- pandas 2.2.2
- numpy 1.26.4
- matplotlib 3.8.4
- seaborn 0.13
- statsmodels 0.14.2
- scikit-learn 1.4.1
- pmdarima 2.1.1

## 5. Reproducibility
- A fixed random_state = 42 is used where applicable.
- All dependencies can be installed using a requirements.txt file.
- Execution environment: Google Colab (ensures consistent setup).


