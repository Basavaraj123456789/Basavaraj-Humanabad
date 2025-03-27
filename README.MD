                                                  ##Sales Forecasting Script Guide 

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

            ##Running the Script
Part 1: Data Processing and Feature Engineering (Day 1)

1. Data Cleaning
- Load the dataset using Pandas.
- Handle missing values in oil prices by filling gaps with interpolation.
- Convert date columns to proper datetime formats.
- Merge data from stores.csv, oil.csv, and holidays_events.csv into the main dataset.

2. Feature Engineering
- Time-based Features:
- Extract day, week, month, year, and day of the week.
- Identify seasonal trends (e.g., are sales higher in December?).

- Event-based Features:
- Create binary flags for holidays, promotions, and economic events.
- Identify if a day is a government payday (15th and last day of the month).
- Consider earthquake impact (April 16, 2016) as a separate feature.

- Rolling Statistics:
- Compute moving averages and rolling standard deviations for past sales.
- Include lagged features (e.g., sales from the previous week, previous month).

- Store-Specific Aggregations:
- Compute average sales per store type.
- Identify top-selling product families per cluster.

3. Exploratory Data Analysis (EDA)
- Visualize sales trends over time.
- Analyze sales before and after holidays and promotions.
- Check correlations between oil prices and sales trends.
- Identify anomalies in the data.

               ##Expected Output
1.Cleaned and merged dataset
2.New features for time-based trends, holidays, promotions, and government paydays
3.Rolling statistics and lagged sales features
4.Sales trend visualization and anomaly detection
5.Correlation analysis between oil prices and sales


                ##Troubleshooting
- If the script fails due to missing libraries, run the `pip install` command above.
- Ensure dataset files are correctly formatted and contain the expected columns.
- Check for missing values after merging datasets to avoid issues during model training.

