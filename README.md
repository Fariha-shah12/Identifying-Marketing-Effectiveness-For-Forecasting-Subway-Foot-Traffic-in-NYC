# 📊 Predicting In-Store Visits from Digital Marketing Channels

This project investigates how different marketing channels impact store visit trends. Using a combination of **machine learning** and **time series forecasting** techniques, we aim to provide data-driven insights for optimizing advertising strategies.

## 📚 Project Overview

* **Goal**: Predict and interpret in-store foot traffic based on marketing metrics such as banner impressions, social media likes, landing page visits, and Google Trends.
* **Techniques Used**:

  * **XGBoost** for supervised regression
  * **SARIMA/Prophet** for forecasting visit trends
  * **SHAP** for explainable AI (feature attribution)
* **Platform**: Databricks (for scalable notebook development and data processing)

## 📅 Dataset

* Collected synthetic campaign effectiveness data
* Features:

  * `banner_imp`: Number of banner ad impressions
  * `social_media_like`: Social media engagement
  * `landing_page_visit`: Visits to campaign landing pages
  * `google_trend`: Google search interest
  * `num_visits`: Actual store visits (target variable)
  * `date`, `day_of_week`, `is_weekend` for time context

## 🔢 Modeling Approach

### XGBoost Regressor

* Trained to predict `num_visits`
* Evaluated using RMSE and R²
* Hyperparameter tuning via `hyperopt`
* SHAP used to assess feature importance

### Time Series Forecasting

* SARIMA and Prophet applied to `num_visits` for future trend predictions
* Seasonal patterns and holidays considered in forecasting

## 📊 Results Summary

| Model   | RMSE     | R² Score |
| ------- | -------- | -------- |
| XGBoost | 59.23    | 0.91     |
| Prophet | \~ 62.14 | --       |

* **Top Features**:

  * Social media likes and landing page visits had the highest SHAP impact.
  * Weekends showed stronger correlation with higher visits due to social engagement.

## 🔹 Key Visuals

* ![SHAP Plot](images/shap_summary.png)
* ![Forecast Plot](images/prophet_forecast.png)
* ![Databricks Flow](images/databricks_architecture.png)

## 📓 Notebooks

* `notebooks/EDA.ipynb` - Data exploration and preprocessing
* `notebooks/XGBoost_Model.ipynb` - Model training and evaluation
* `notebooks/SHAP_Interpretation.ipynb` - Feature attribution
* `notebooks/Prophet_SARIMA_Forecasting.ipynb` - Time series analysis

## 🚀 Getting Started

```bash
# Clone the repo
https://github.com/Fariha-shah12/campaign-foot-traffic

# Install dependencies
pip install -r requirements.txt
```

## 🔗 Connect

* [LinkedIn](https://linkedin.com/in/shahfariha)
* [Medium Articles](https://medium.com/@FarihaShah)

---

**Note**: All data used is simulated and does not contain any real personal information.

> "Marketing decisions should be backed by data, not assumptions."

---

💍 Star this repo if you find it useful!

---
