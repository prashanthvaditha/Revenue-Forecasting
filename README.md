## Revenue Forecasting using ARIMA, SARIMA, and SARIMAX

### Overview

This notebook demonstrates time series demand forecasting using ARIMA (Autoregressive Integrated Moving Average), SARIMA (Seasonal ARIMA), and SARIMAX (SARIMA with Exogenous Regressors) models. It uses a dataset of daily revenue, discount rates, and coupon rates to predict future revenue.

### Contents

1.  **Useful Functions:**
    *   `model_assessment(train, test, predictions, chart_title)`:  Visualizes the train, test, and predicted data, and calculates MAE (Mean Absolute Error), RMSE (Root Mean Squared Error), and MAPE (Mean Absolute Percentage Error) to assess model performance.
    *   `plot_future(y, forecast, title)`: Plots the historical data along with the forecasted values.

2.  **Libraries and Data:**
    *   Imports necessary Python libraries, including `pandas`, `matplotlib`, `statsmodels`, `sklearn`, and `pmdarima`.
    *   Loads the `daily_revenue.csv` dataset, setting the 'date' column as the index and parsing dates.

3.  **Data Exploration and Preprocessing:**
    *   Loads the daily revenue data from the CSV file.
    *   Sets the date as the index and parses the dates.
    *   Displays the first few rows of the dataframe.

4.  **Model Building and Evaluation:**
    *   Splits the data into training and testing sets.
    *   Explores and applies ARIMA, SARIMA, and SARIMAX models.
    *   Uses functions to assess model performance (MAE, RMSE, MAPE) and visualize results.

### Data Description

The `daily_revenue.csv` file contains the following columns:

*   **date:** Date of the observation.
*   **revenue:** Daily revenue.
*   **discount\_rate:** Discount rate applied on that day.
*   **coupon\_rate:** Coupon rate applied on that day.

### Usage

1.  **Mount Google Drive:** The notebook is designed to be run in Google Colab and starts by mounting your Google Drive to access the data file.
2.  **Install Libraries:**  The notebook installs the `pmdarima` library using `pip`.
3.  **Data Loading and Preparation:** The notebook reads the `daily_revenue.csv` file into a Pandas DataFrame, sets the 'date' column as the index, and parses the dates.
4.  **Model Implementation:**  The notebook provides code snippets for implementing ARIMA, SARIMA, and SARIMAX models.  You can modify the model parameters (p, d, q, P, D, Q, s) to find the best fit for your data.
5.  **Model Assessment:** The `model_assessment` function helps evaluate the performance of your model by calculating MAE, RMSE, and MAPE.  Visualizations are also provided to compare the predicted values against the actual values.
6.  **Forecasting:** The `plot_future` function helps visualize the forecasted revenue for future dates.

### Models Implemented

*   **ARIMA:** A basic time series forecasting model.
*   **SARIMA:** An extension of ARIMA to handle seasonality in time series data.
*   **SARIMAX:**  An extension of SARIMA that includes exogenous variables (like discount rate and coupon rate) to improve forecasting accuracy.

### Key Observations and Potential Improvements

*   The notebook explores different ARIMA model configurations and assesses their performance.
*   The SARIMAX model incorporates discount and coupon rates as exogenous variables, potentially improving forecast accuracy.
*   Further improvements could involve:
    *   More extensive hyperparameter tuning for each model.
    *   Feature engineering to create new relevant exogenous variables.
    *   Evaluating the models on different time periods to ensure robustness.





