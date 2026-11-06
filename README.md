# Electricity Consumption Forecasting

Time series forecasting project using **Python, Pandas, and XGBoost** to predict hourly electricity demand based on historical consumption data.

## Dataset

[Hourly Energy Consumption — Kaggle](https://www.kaggle.com/datasets/robikscube/hourly-energy-consumption)

Historical hourly electricity consumption data from the PJM East region.

## Tech Stack

Python · Pandas · NumPy · Matplotlib · Scikit-learn · XGBoost · Jupyter Notebook

## Methodology

- **EDA:** Analyzed hourly, daily, and seasonal electricity consumption patterns.
- **Feature Engineering:** Extracted calendar features and historical demand lags (24h and 168h).
- **Model Training:** Trained two XGBoost regressors with and without lag features.
- **Evaluation:** Compared models using MAE, RMSE, and Actual vs. Predicted visualizations.
- **Validation:** Used a chronological train/test split (before and after January 1, 2017).

## Project Structure

```text
├── data/
│   └── dataset.csv
├── TSA.ipynb
├── requirements.txt
└── README.md
```

## How to Run

```bash
pip install -r requirements.txt
jupyter notebook TSA.ipynb
```

## Limitations

The lag-based model assumes historical demand observations are available when making predictions. Weather and holiday information are not included.