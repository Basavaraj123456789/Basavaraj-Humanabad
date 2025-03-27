                                     ## Sales Forecasting Script Guide ##

                    ##Overview
This script performs sales forecasting using various data sources, including store information, oil prices, and holiday events. It includes data preprocessing, feature engineering, and preparation for model training.

                 ##Prerequisites
Before running the script, ensure you have the following installed:
- Python (>=3.8)
- Required libraries:
  ```bash
  pip install pandas numpy matplotlib seaborn statsmodels scikit-learn xgboost tensorflow
  ```
- Dataset files:
  - `train.csv`
  - `test.csv`
  - `stores.csv`
  - `oil.csv`
  - `holidays_events.csv`

              ## Running the Script
1. **Load Data:** The script reads CSV files into Pandas DataFrames.
2. **Data Preprocessing:**
   - Converts date columns to datetime format.
   - Fills missing values in oil prices using interpolation.
   - Merges all datasets based on common keys.
3. **Feature Engineering:**
   - Extracts time-based features (day, month, year, etc.).
   - Creates holiday-related indicators.
   - Computes rolling statistics (lag, moving averages, etc.).
   - Generates store-specific aggregate features.
4. **Execution:**
   - Run the script using:
     ```bash
     python sales_forecasting.py
     ```
   - Ensure all dataset files are in the same directory as the script.

                  ## Expected Output
The script will output a processed dataset ready for machine learning models. Further steps involve training models like ARIMA, RandomForest, or LSTM using the prepared data.

                     ## Troubleshooting
- If the script fails due to missing libraries, run the `pip install` command above.
- Ensure dataset files are correctly formatted and contain the expected columns.
- Check for missing values after merging datasets to avoid issues during model training.

