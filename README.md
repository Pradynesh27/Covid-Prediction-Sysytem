# Covid-Prediction
# COVID-19 Case Trend Prediction

This project focuses on predicting the spread of COVID-19 by analyzing historical infection data. Using time-series forecasting techniques and machine learning regression models, the project identifies patterns in case growth to help visualize and predict future trends.

## Key Results
* **Best Model:** Random Forest Regressor
* **Validation Strategy:** TimeSeriesSplit (to respect the temporal nature of the data)
* **Optimization:** Hyperparameter tuning via `RandomizedSearchCV`
* **Metrics:** Evaluated using RMSE, MAE, and $R^2$ Score to ensure robust predictive power.

## Dataset Features
The dataset includes global COVID-19 statistics:
- **Province/State & Country/Region:** Geographical identifiers.
- **Lat/Long:** Precise location coordinates.
- **Date Columns (Time-Series):** Daily cumulative case counts starting from January 2020.

## Tech Stack
- **Language:** Python
- **Data Manipulation:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-Learn (Random Forest, XGBoost, Gradient Boosting, Logistic Regression)

## Project Workflow
1. **Data Cleaning & Reshaping:** Transformed the wide-format time-series data into a long format suitable for supervised machine learning.
2. **Feature Engineering:** Extracted temporal features and handled geographical encoding.
3. **Model Training:** Developed several regression pipelines:
   - Random Forest Regressor (Selected as the top performer)
   - XGBoost Regressor
   - Gradient Boosting Regressor
4. **Hyperparameter Tuning:** Fine-tuned `n_estimators`, `max_depth`, and `learning_rate` using `RandomizedSearchCV` to minimize error.
5. **Evaluation:** Assessed model generalization using time-aware cross-validation to prevent data leakage from the future into the past.

## Conclusion
The Random Forest model demonstrated the strongest ability to capture the non-linear growth patterns of the pandemic. The project highlights the importance of scaling features and using time-specific validation splits when dealing with global health crisis data.
