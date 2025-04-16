# 🏠 House Price Prediction Model

A comprehensive machine learning project comparing multiple regression models to predict house prices with thorough performance analysis.

## 📌 Overview

This project evaluates various regression models (Linear Regression, Ridge/Lasso, KNN, Random Forest, SVR) to determine the optimal approach for predicting house prices based on key features like square footage, location, and property grade.

## 📊 Key Findings

### Best Performing Model
**Model 0 (Linear Regression with All Features)**  
✅ **R²**: 0.89 | **RMSE**: 0.1726  
- Dominant features: `sqft_living`, zip codes, and `grade`  
- Outperformed all alternatives in accuracy and interpretability

### Critical Insights
1. Location features (zip codes) contribute **33% of explanatory power**  
2. Feature engineering (`sqft_grade`) improved parsimonious models  
3. Regularization (Ridge) helped but couldn't surpass full-feature linear regression  
4. Non-linear models (Random Forest) underperformed compared to linear approaches

## 🛠️ Technical Implementation

### Models Tested
| Model Type          | Best R² | Best RMSE | Key Observation |
|---------------------|---------|-----------|-----------------|
| Linear Regression   | 0.890   | 0.1726    | Best overall    |
| Ridge Regression    | 0.567   | 0.3423    | Best regularized|
| Random Forest       | 0.510   | 0.3643    | Best non-linear |
| SVR (Linear Kernel) | Failed  | -         | Scaling needed  |

### Feature Importance (Top 3)
1. `sqft_living` (Baseline model)  
2. `zip codes` (Location data)  
3. `sqft_grade` (Engineered feature)  

## 🚀 How to Use

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/house-price-prediction.git
