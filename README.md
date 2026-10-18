# used-phones-

Exploratory data analysis and regression modeling of used and refurbished phone and tablet prices, using pandas, numpy, matplotlib and statsmodels.

## Dataset
The dataset contains 3,454 used and refurbished phones and tablets released between 2013 and 2020, with 15 variables describing each device. The target variable is `normalized_used_price`. The data and its metadata were provided as part of the GSBA-594 coursework.

## Files
| File | Description |
|---|---|
| `Data Analysis Assignment Used Phones.ipynb` | Jupyter Notebook with the code, outputs, charts and comments |
| `used_device_data.csv` | Dataset of 3,454 used devices: brand, OS, screen size, cameras, memory, RAM, battery, weight, release year, days used, and normalized new and used prices |

## What the notebook covers
1. Data limitations: missing values, skewed variables, imbalanced categories and suspicious values
2. Outlier detection with box plots (1.5 × IQR rule)
3. A new `device_age` feature
4. Descriptive statistics with numpy: mean, min, max, standard deviation, variance and percentiles
5. Random sampling of 500 devices
6. Z-score outliers in used price, compared with the whole dataset
7. Multiple linear regression (statsmodels OLS) of used price on internal memory, battery, weight, days used and 5G
8. Scatterplots with regression lines for each predictor

## Key findings
- Battery capacity and 5G are the strongest predictors of used price; each extra year of use lowers the predicted price by about 0.07 normalized units.
- The model explains about 42% of the variation in used price (R² = 0.424).
- Weight is positively related to price on its own, but not significant once battery is held constant (the two are correlated, r = 0.70).
- The 35 price outliers split into cheap older feature phones and expensive recent flagships.

## How to run
1. Install Anaconda (includes Python, pandas, numpy, matplotlib and statsmodels).
2. Keep the notebook and `used_device_data.csv` in the same folder.
3. Open the notebook in Jupyter and select **Kernel → Restart Kernel and Run All Cells**.
