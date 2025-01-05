# Temple Footfall Analysis: A Time series study

# Temple Footfall Analysis

## Overview
This repository contains a comprehensive time series analysis of temple visitor patterns using advanced statistical methods and machine learning approaches. The study analyzes 1,096 observations from 2016 to early 2019, exploring relationships between visitor patterns and real-world influences such as festivals, weekends, and weather events.

## Key Features
- **Time Series Analysis**: Includes stationarity testing, autocorrelation analysis, and seasonal decomposition
- **Statistical Modeling**: Implements SARIMAX, Prophet, XGBoost, and VAR models
- **Pattern Recognition**: Utilizes PCA and visitor segmentation analysis
- **Predictive Analytics**: Features multiple forecasting models with comparative performance metrics

## Model Performance

| Model    | MAE   | RMSE  | R² Score |
|----------|-------|-------|----------|
| SARIMAX  | 11.89 | 14.33 | 0.91     |
| Prophet  | 12.06 | 14.50 | 0.91     |
| XGBoost  | 13.23 | 16.28 | 0.89     |
| VAR      | 34.74 | 46.31 | 0.08     |

## Key Findings

### Visitor Patterns
- Average weekend footfall: 112.31 visitors
- Average weekday footfall: 82.07 visitors
- Significant weekend effect confirmed (t-statistic: 10.8212, p-value: 0.0001)

### Traffic Segmentation
- Base Traffic: 30-70 visitors/day (routine visitors)
- Medium Traffic: 70-120 visitors/day (local festivals)
- Peak Traffic: 150-250 visitors/day (major festivals)

## Technical Details

### Data Preprocessing
- Outlier handling: 51 anomalies identified and capped within [-21.00, 189.00]
- Distribution: Non-normal (Shapiro-Wilk Test: 0.8834, p < 0.0001)
- Stationarity: Confirmed via ADF test (statistic = -4.4187, p = 0.0003)

### Feature Engineering
Key predictive features include:
- Previous day footfall (footfall_lag_1)
- 4-day lagged footfall (footfall_lag_4)
- 7-day lagged footfall (footfall_lag_7)
- Day of month (for festival patterns)

## Contributing
Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## Future Work
- Integration of deep learning models (LSTM + SARIMAX hybrid)
- Ensemble modeling approaches
- Extension to other cultural and seasonal phenomena

## Contact
Harsh Joshi - joshiharsh0506@gmail.com
