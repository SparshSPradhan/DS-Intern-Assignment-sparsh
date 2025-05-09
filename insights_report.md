
# Smart Factory Energy Prediction: Insights and Recommendations

## Approach
We conducted exploratory data analysis to understand sensor data patterns, preprocessed the data by handling missing values and extracting time-based features, and split the data chronologically to respect its time series nature. Feature selection was performed using Random Forest importance, and two models (Random Forest and XGBoost) were trained and evaluated using RMSE, MAE, and R² metrics.

## Key Findings
- **Feature Importance**: Environmental factors such as temperature and humidity in specific zones (e.g., zone1_temperature, zone1_humidity) significantly influence energy consumption.
- **Random Variables**: Random_variable1 and random_variable2 exhibited low correlation and importance, indicating they are likely not useful for prediction.
- **Temporal Patterns**: Energy consumption varies by hour, day of week, and month, suggesting opportunities for time-based optimization.

## Model Performance
- The Random Forest model demonstrated robust performance with low RMSE and high R², indicating reliable predictions.
- Cross-validation with TimeSeriesSplit confirmed model stability across different temporal splits.

## Recommendations
1. **Optimize Environmental Conditions**: Adjust temperature and humidity in high-impact zones to minimize energy usage, such as improving insulation or HVAC efficiency.
2. **Schedule Operations**: Shift high-energy tasks to off-peak hours or days (e.g., weekends if lower consumption is observed) based on temporal patterns.
3. **Monitor Key Sensors**: Prioritize maintenance and calibration of sensors in critical zones to ensure accurate data for energy management.
4. **Exclude Random Variables**: Discontinue collecting random_variable1 and random_variable2 to streamline data collection, as they add little predictive value.

## Limitations
- The model relies on historical sensor data and assumes consistent data quality; outliers or sensor failures could affect predictions.
- Generalization to other facilities may require retraining with site-specific data.
- The model does not account for sudden operational changes or external factors like equipment upgrades.
    