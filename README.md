# Weekly Grocery Expenditure Forecasting

## Project Overview

This project focuses on forecasting the next week's grocery expenditure using historical weekly grocery spending data. It explores simple time-series forecasting techniques and evaluates their prediction errors.

## Objective

To analyze weekly grocery expenditure and estimate the expenditure for the following week using historical spending patterns.

## Dataset

The dataset contains 8 consecutive weeks of grocery expenditure records.

**File:** `data/weekly_expenditure_data.csv`

The dataset includes:
- Week number
- Week start and end dates
- Grocery expenditure in Indian rupees (INR)
- Number of purchases
- Notes about the week's purchases

Some expenditure values were recalled from memory, so the dataset may not be fully receipt-verified.

## Methodology

1. Load and inspect the dataset.
2. Check data types, missing values, duplicate records, and weekly date intervals.
3. Visualize weekly grocery expenditure and calculate week-to-week changes.
4. Apply two baseline forecasting methods:
   - **Naive forecasting:** Uses the latest observed week's expenditure as the next prediction.
   - **Mean forecasting:** Uses the average expenditure of the available historical weeks.
5. Evaluate predictions using chronological walk-forward validation and Mean Absolute Error (MAE).

## Results

The following results were obtained using the current dataset and notebook:

| Forecasting method | MAE |
|---|---:|
| Naive forecasting | ₹415.00 |
| Mean forecasting | ₹212.60 |

The evaluation used only 3 test observations, so these results should be interpreted cautiously.

The mean forecasting method had a lower MAE in this small evaluation. More data is needed to determine whether this performance generalizes to future weeks.

## Limitations

- Only 8 weeks of observations are available.
- Some expenditure values were recalled from memory.
- The evaluation contains only 3 test observations.
- The forecasts are basic benchmarks and may not capture seasonal patterns or changes in household spending.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Jupyter Notebook
- Scikit-learn
- Statsmodels

## Future Improvements

- Collect more weeks of expenditure data.
- Verify spending amounts against receipts or transaction records where available.
- Compare additional forecasting methods when sufficient data is available.
- Evaluate predictions on a larger chronological test set.

## Project Status

Academic learning project — baseline forecasting and evaluation completed; further data collection and improvements are possible.

