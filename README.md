# Coral Bleaching Prediction Dashboard (R.E.E.F.)
Machine learning dashboard for predicting coral reef bleaching using environmental and climate data.

## Overview
This project develops a machine learning enabled early warning system for coral reef bleaching.

It integrates multi source environmental data, applies advanced preprocessing and spatial interpolation, and delivers predictions through an interactive Streamlit dashboard to support conservation decision making.

The system is designed to shift coral monitoring from reactive reporting to proactive, data driven intervention.

---

## Project Background
Coral reefs support over 25 percent of marine biodiversity but are increasingly threatened by climate change and environmental stress.

This project was developed as part of the MSc in Business Analytics at Cork University Business School and focuses on building an operational predictive analytics pipeline for reef conservation.

---

## Objectives
The main objectives of this project were:

- Integrate heterogeneous oceanographic and reef monitoring datasets
- Address missing and sparse data through robust imputation and interpolation
- Build accurate and interpretable prediction models
- Develop an interactive early warning dashboard
- Provide actionable insights for conservation stakeholders

---

## Datasets
The project uses multiple public scientific datasets:

- BCO-DMO Reef Check Dataset (1997 to 2022)
- GLODAP Ocean Biogeochemical Dataset
- ICRI Coral Restoration Database (contextual analysis)

Final integrated dataset:
- 32,737 records
- 82 countries
- 8 oceanic regions
- Time span: 2000 to 2019

Key features include:
Sea surface temperature, cyclone frequency, dissolved oxygen, pH, alkalinity, turbidity, depth, and thermal stress indicators.

---

## Tools and Technologies
- Python (Pandas, NumPy, Scikit learn)
- XGBoost, LightGBM
- Streamlit
- Jupyter Notebook
- GeoPy
- Matplotlib and Seaborn
- Git and GitHub

---

## Methodology

### 1. Data Preprocessing
- Removal of non informative variables
- Missing value treatment using:
  - MICE imputation
  - Median and linear interpolation
- Geolocation tagging using GeoPy
- Feature scaling

### 2. Data Integration
- Spatial temporal matching using KD Tree and H3 indexing
- 4D Inverse Distance Weighting (IDW) interpolation
- Integration of secondary environmental variables

### 3. Exploratory Analysis
- Distribution and outlier analysis
- Correlation and multicollinearity checks
- Geographic hotspot mapping
- Temporal trend analysis

### 4. Modelling
Regression Models:
- ExtraTrees Regressor
- Random Forest
- Gradient Boosting
- Linear Models

Classification Models:
- XGBoost
- LightGBM
- Random Forest
- KNN with SMOTE

Time Series:
- SARIMA
- Prophet
- Trend based projections

Model interpretability was supported using SHAP analysis.

### 5. Dashboard Development
- Initial prototype in Tableau
- Final implementation in Streamlit
- Integrated ML inference pipeline
- User focused design iterations

---

## Results

### Regression Performance
- Best models: ExtraTrees and Random Forest
- R² ≈ 0.67
- RMSE ≈ 10

### Classification Performance
- Best model: XGBoost
- Accuracy ≈ 89 percent
- Macro F1 ≈ 0.67

### Key Drivers Identified
- Sea surface temperature
- Cyclone frequency
- Thermal stress
- Dissolved oxygen
- Turbidity

Ensemble tree based models consistently outperformed linear and distance based approaches.

---

## Dashboard Features (R.E.E.F.)

The Streamlit dashboard provides:

- KPI summary cards
- Global bleaching trend analysis
- SHAP feature importance
- Region and year forecasting
- Interactive scenario predictor
- Severity gauge
- Bulk CSV prediction upload
- Automated feature validation

Users can perform what if analysis and generate region specific conservation recommendations.

---

## Live Dashboard
(To be added after deployment)

🔗 [https://reef-dashboard.streamlit.app/](url)
