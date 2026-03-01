
Renewable energy Production Forecasting

This project forecasts solar and wind energy production in France using historical daily data and machine learning. The model uses a Random Forest Regressor to predict daily production based on date features.


## Dataset

The dataset (`intermittent-renewables-production-france.csv`) contains:

 `Date and Hour` – Timestamp of measurement
`Source` – Energy source (`Solar` or `Wind`)
 `Production` – Energy produced 

Preprocessing steps:

1. Convert timestamps to `datetime` objects.
2. Resample hourly data into **daily totals**.
3. Extract `day`, `month`, and `year` as features for prediction.



Project Structure

Data Preprocessing:

Split the dataset into Solar and Wind subsets
Aggregate production by day
Generate date features for regression (`day`, `month`, `year`)

Machine Learning Model:

 Model: `RandomForestRegressor` (from `sklearn.ensemble`)
 Training/Test split: 80% train, 20% test
 Features: `year`, `month`, `day`
 Target: `Production`

Evaluation Metrics:

 Root Mean Squared Error (RMSE)
 Mean Absolute Error (MAE)

Visualization:
<img width="1200" height="500" alt="Figure_1" src="https://github.com/user-attachments/assets/1fa3a8cc-e61f-40d0-a3c2-c69866d9e9c2" />

<img width="1200" height="500" alt="Figure_2_wind" src="https://github.com/user-attachments/assets/2fd4b844-1987-4521-a802-b589cc01db7e" />




Usage

1. Install the required Python packages:


pip install numpy pandas matplotlib scikit-learn


2. Place the dataset `intermittent-renewables-production-france.csv` in the project directory.

3. Run the Python script:


4. The script will:

   * Train separate models for solar and wind production
   * Plot actual vs. predicted production
   * Output RMSE and MAE metrics for each model

