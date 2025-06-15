# Prediction-of-Sugarcane-Yield-Using-ML-Models

## 📌 Project Overview

This project aims to **predict sugarcane yield** using **satellite-based vegetation indicators** across 12 months. We use two ensemble machine learning models — **Random Forest (RF)** and **Gradient Boosting Regressor (GBR)** — to train predictive models on a feature set of 72 remote sensing variables.

---

## 📊 Dataset

- **Target Variable:** `SUGARCANE YIELD (Kg per ha)`
- **Features (72 total):** Monthly means of:
  - NDVI (Normalized Difference Vegetation Index)
  - EVI (Enhanced Vegetation Index)
  - LAI (Leaf Area Index)
  - GPP (Gross Primary Production)
  - ET (Evapotranspiration)
  - FPAR (Fraction of Photosynthetically Active Radiation)
- **Time Range:** 12 months (April to March), e.g.:
  - `Apr_NDVI Mean`, `May_ET Mean`, ..., `Mar_GPP Mean`




## 🎯 Objectives

- Use **all 72 features** to train ensemble models to predict sugarcane yield.
- Evaluate performance of:
  - Random Forest Regressor
  - Gradient Boosting Regressor
- Compare performance using R², MSE, MAE, and cross-validation.
  

---

## 🧪 Methodology

### 1. **Data Preparation**
- Features: All 72 satellite-based monthly variables.
- Target: Sugarcane yield.
- Splitting: 80% training, 20% testing.

### 2. **Model Training**
- **Random Forest Regressor**
  - Ensemble of decision trees with bagging.
  - Good for handling high-dimensional, non-linear data.
- **Gradient Boosting Regressor**
  - Ensemble of weak learners trained sequentially.
  - Usually more accurate but can overfit on small/noisy data.

### 3. **Model Evaluation**
- Metrics used:
  - R² (coefficient of determination)
  - MSE (mean squared error)
  - MAE (mean absolute error)
  - Cross-validation scores

### 4. **Feature Importance**
- Ranked the top features influencing yield predictions.
RANDOM FOREST
<img width="547" alt="{46FE06A6-9CD0-47D9-BF0D-965D673B3054}" src="https://github.com/user-attachments/assets/85ae2013-2bb6-4204-bbb4-87459269970a" />

GRADIENT BOOSTING RADIANT
<img width="514" alt="{C819542A-B652-4999-94DA-CD8E5020F0A4}" src="https://github.com/user-attachments/assets/bb6ee31c-2c9e-4ad8-84fa-3361bf89a6af" />









## ⚙️ Tools & Libraries

- **Python 3.10+**
- `pandas`, `numpy`
- `scikit-learn`
- `shap`
- `matplotlib`, `seaborn`

---

## 📈 Results

| Model         | R² Score | RMSE        | MAE         | Cross-Validated R² |
|---------------|----------|-------------|-------------|--------------------|
| Random Forest | ~0.52    | ~588.692    | ~467.19     | ~0.65              |
| GBR           | ~0.59    | ~542 .641   | ~421.56     | ~0.68              |

> Gradient Boosting slightly outperformed Random Forest. Both models showed good predictive power using all features.

---



