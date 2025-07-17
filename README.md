# Prediction-of-Sugarcane-Yield-Using-ML-Models

## 📌 Project Overview

This project aims to **predict sugarcane yield** using **satellite-based vegetation indicators** across 12 months. Two ensemble machine learning models -" **Random Forest (RF)** and **Gradient Boosting Regressor (GBR)**" were used  to train predictive models on a feature set of 72 remote sensing variables.

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


---

## 🎯 Objectives

- Use **all 72 features** to train ensemble models to predict sugarcane yield.
- Evaluate performance of:
  - Random Forest Regressor
  - Gradient Boosting Regressor
- Compare performance using R², MSE, MAE, and cross-validation.
  

---

## 🧪 Methodology

### 1. **Data preparation**
- Features: All 72 satellite-based monthly variables.
- Target: Sugarcane yield.
- Splitting: 80% training, 20% testing.

### 2. **Model Training**
- **Random Forest Regressor**

- <img width="462" alt="{8E388E4C-C2AC-4610-9EC0-582F68E88686}" src="https://github.com/user-attachments/assets/bb59a7a3-31d3-408d-ae8a-5497c95df1d1" />


  -Best Parameters used: {'n_estimators': 100, 'min_samples_split': 2, 'min_samples_leaf': 2, 'max_depth': 10, 'bootstrap': True}
  
- **Gradient Boosting Regressor**

<img width="463" alt="{36737836-B959-40F1-84EE-833DED73D655}" src="https://github.com/user-attachments/assets/fdfb9d86-4904-4875-8190-d7e4ac4f77a5" />

  -Best Parameters used: {'n_estimators': 100, 'min_samples_split': 2, 'min_samples_leaf': 1, 'max_depth': 4, 'learning_rate': 0.05}


### 3. **Model Evaluation**
- Metrics used:
  - R² (coefficient of determination)
  - MSE (mean squared error)
  - MAE (mean absolute error)
  - Cross-validation scores

### 4. **Feature Importance**
- Ranked the top features influencing yield predictions.

- 
RANDOM FOREST

<img width="541" alt="{AC1DC611-6A86-4547-BE7F-0FCF524DE515}" src="https://github.com/user-attachments/assets/3e627cc8-4ba2-4fc6-ae75-e4b094d56e3a" />




---

-GRADIENT BOOSTING RADIANT

<img width="514" alt="{F6C33CE1-2450-4551-BE07-899063AF7B3E}" src="https://github.com/user-attachments/assets/40fdbeb6-2eab-4b13-8a9e-3b57a96503bd" />





---

## ⚙️ Tools & Libraries

- **Python 3.10+**
- `pandas`,
-  `numpy`
- `scikit-learn`
- `matplotlib`,
- `seaborn`

---

## 📈 Results

| Model         | R² Score | RMSE        | MAE         | Cross-Validated R² |
|---------------|----------|-------------|-------------|--------------------|
| Random Forest | ~0.52    | ~588.692    | ~467.19     | ~0.65              |
| GBR           | ~0.59    | ~542 .641   | ~421.56     | ~0.68              |

> Gradient Boosting slightly outperformed Random Forest. Both models showed good predictive power using all features.

---

## Discussion
The  yield for the 15 districts  of western  Uttar Pradesh is esti
mated in this project by using historic monthly means of
 satellite data as predictors. Regression was carried out
 using the  RF and  GBR algorithms. The GBR
 model outruns RF with an R^2 of 0.59 and
 an RMSE of  542.641. The  MODIS
 products such as FPAR, LAI, NDVI, GPP and others have reasonable potential to
 estimate pre-harvest yield with reasonable accuracies. FPAR and  LAI are the most important features in both the models for prediction following by others.These
 variables directly control the photosynthetic process and
 denote a good measure of the biomass accumulation in
 crops, thus offering better predictions.
 



