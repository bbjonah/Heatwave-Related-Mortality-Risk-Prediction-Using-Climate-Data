# 🌡️ Heatwave-Related Mortality Risk Prediction

A machine learning system for predicting mortality risk during heatwave events using climate, environmental, and demographic data.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Objectives](#objectives)
- [Problem Statement](#problem-statement)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Machine Learning Approach](#machine-learning-approach)
- [Feature Engineering](#feature-engineering)
- [Model Evaluation](#model-evaluation)
- [Results & Visualizations](#results--visualizations)
- [Future Improvements](#future-improvements)
- [Applications](#applications)
- [License](#license)

---

## Overview

This project uses climate, environmental, and demographic data to predict mortality risk during heatwave events using supervised machine learning. The system analyzes weather patterns and public health indicators to identify periods of elevated mortality risk caused by extreme heat conditions.

The project demonstrates how data science and machine learning can support **public health preparedness** and **climate adaptation strategies**.

---

## Objectives

- Predict mortality risk levels (Low / Moderate / High) during heatwave periods
- Analyze relationships between temperature extremes and mortality outcomes
- Identify the most influential climate and demographic variables
- Build and evaluate a robust machine learning classification model
- Provide actionable insights for public health early warning systems

---

## Problem Statement

Heatwaves are increasing in frequency due to climate change and are associated with elevated risks of:

- Heat stroke
- Cardiovascular diseases
- Respiratory illnesses
- Dehydration
- Increased mortality among vulnerable populations

Public health agencies require predictive systems to forecast periods of high mortality risk, enabling better emergency response and healthcare resource allocation.

---

## Dataset

This project uses a **synthetic dataset** generated for research and educational purposes.

### Features

| Feature | Description |
|---|---|
| `date` | Observation date |
| `max_temperature_c` | Daily maximum temperature (°C) |
| `min_temperature_c` | Daily minimum temperature (°C) |
| `avg_temperature_c` | Daily average temperature (°C) |
| `humidity_percent` | Relative humidity (%) |
| `wind_speed_kmh` | Wind speed (km/h) |
| `rainfall_mm` | Daily rainfall (mm) |
| `pm25_air_pollution` | PM2.5 air pollution level |
| `uv_index` | UV radiation index |
| `heat_index` | Apparent temperature |
| `elderly_population_pct` | Percentage of elderly population |
| `population_density` | Population density |
| `poverty_index` | Poverty indicator |
| `heatwave` | Heatwave occurrence (0/1) |
| `consecutive_heat_days` | Consecutive heatwave days |
| `mortality_count` | Daily mortality count |
| `mortality_risk_level` | **Target:** Mortality risk category |

### Heatwave Definition

> A heatwave is defined as **T_max > 35°C for ≥ 3 consecutive days**.

---

## Project Structure

```
heatwave-mortality-project/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   ├── eda.ipynb
│   └── modeling.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── feature_engineering.py
│   ├── train_model.py
│   └── evaluate.py
│
├── models/
├── outputs/
├── requirements.txt
├── README.md
└── heatwave_mortality_synthetic_dataset.csv
```

---

## Installation

**1. Clone the repository:**

```bash
git clone https://github.com/yourusername/heatwave-mortality-project.git
cd heatwave-mortality-project
```

**2. Install dependencies:**

```bash
pip install -r requirements.txt
```

**Requirements:**

```
pandas
numpy
matplotlib
seaborn
scikit-learn
joblib
```

---

## Usage

Run the full prediction pipeline:

```bash
python heatwave_prediction.py
```

Or explore interactively via the provided notebooks:

```bash
jupyter notebook notebooks/eda.ipynb
jupyter notebook notebooks/modeling.ipynb
```

---

## Machine Learning Approach

**Task type:** Supervised multi-class classification

**Target variable:** `mortality_risk_level`

| Class | Description |
|---|---|
| `Low` | Minimal mortality risk |
| `Moderate` | Elevated mortality risk |
| `High` | Critical mortality risk |

**Algorithm:** Random Forest Classifier

```python
from sklearn.ensemble import RandomForestClassifier

model = RandomForestClassifier(
    n_estimators=200,
    max_depth=10,
    random_state=42
)
```

### Project Workflow

```
Data Collection → Data Cleaning → EDA → Feature Engineering
→ Model Training → Evaluation → Feature Importance → Deployment
```

---

## Feature Engineering

Additional features engineered from raw data:

- **Temperature range** — difference between daily max and min temperature
- **Heatwave indicators** — binary flags for threshold exceedance
- **Consecutive hot days** — rolling count of days above threshold
- **Time-based features** — month, year, and day of year

---

## Model Evaluation

The model is evaluated using the following metrics:

| Metric | Description |
|---|---|
| Accuracy | Overall correct predictions |
| Precision | Correctness of positive predictions |
| Recall | Coverage of actual positives |
| F1-score | Harmonic mean of precision and recall |
| Confusion Matrix | Class-level prediction breakdown |

---

## Results & Visualizations

The project includes the following analyses and visualizations:

- Temperature distribution analysis
- Mortality distribution across risk levels
- Correlation heatmap of climate variables
- Feature importance chart
- Confusion matrix

---

## Future Improvements

- **Real-time data** — Integration with live weather APIs
- **Deep learning** — LSTM models for time-series forecasting
- **Geographic mapping** — Spatial risk visualization by region
- **Explainability** — SHAP values for model interpretability
- **Climate scenarios** — Forecasting under different climate change projections
- **Dashboard** — Public health monitoring and alert dashboard

---

## Applications

This system is useful for:

- Public health agencies
- Climate and environmental researchers
- Hospitals and emergency response teams
- Epidemiologists and biostatisticians
- Urban planners and policymakers
- Environmental health analysts

---

## License

This project is open-source and available under the [MIT License](LICENSE).

---

## Author

**Buka Jonah**


Developed as a **Public Health Data Science and Machine Learning** project focused on climate-health risk prediction.
