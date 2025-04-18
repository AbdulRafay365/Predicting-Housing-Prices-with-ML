# 🏡 Predicting Housing Prices in King County, Washington

A Comparative Analysis of Machine Learning Models for Accurate Price Estimation

![Blog-Banners-min-11-980x490](https://github.com/user-attachments/assets/490cf8fa-1e18-479d-a51e-96eeed5e3b7b)

## 📊 Project Overview

This project explores a dataset of real estate properties in King County, WA, and applies various machine learning regression techniques to predict housing prices. Using models such as Linear Regression, Ridge, Lasso, and KNN, we evaluate their performance and interpret the significance of different housing features.

The objective is to determine the most effective model for accurate house price prediction and understand the impact of various predictors like square footage, grade, bathrooms, and location.

---

## 📁 Dataset

- **Source**: [Kaggle - House Sales in King County, USA](https://www.kaggle.com/harlfoxem/housesalesprediction)
- **Rows**: 21,613  
- **Columns**: 21 (including `price`, `bedrooms`, `bathrooms`, `sqft_living`, `zipcode`, etc.)

---

## 🛠️ Project Workflow

1. **Data Preprocessing**
   - Converted `date` to datetime and extracted year/month/day
   - One-hot encoded `zipcode`, `view`, and `waterfront`
   - Removed outliers and unrealistic entries (e.g., 33 bedrooms)
   - Applied log transformation to `price`

2. **Exploratory Data Analysis (EDA)**
   - Boxplots, histograms, scatter plots
   - Correlation analysis with `log_price`
   - Visual comparison before and after log transformation

3. **Model Building**
   - **Model 0**: Linear Regression (all features)
   - **Model 1**: Linear Regression (selected features)
   - **Model 2**: Model 1 + `sqft_living15`
   - **Ridge Regression**: Regularized with interaction and polynomial terms
   - **Lasso Regression**: For feature selection and regularization
   - **KNN Regression**: k=5 and k=10 evaluated

4. **Model Evaluation**
   - Metrics: MAE, MSE, RMSE, R²
   - 5-Fold Cross-validation
   - GridSearchCV for best alpha in Ridge

---

## 📈 Results Summary

| Model               | RMSE    | MAE    | R² Score |
|--------------------|---------|--------|----------|
| Linear Regression (All Features) | **0.1726** | 0.1284 | **0.8900** |
| Model 1            | 0.3464  | 0.2796 | 0.5570   |
| Model 2            | 0.3447  | 0.2794 | 0.5612   |
| Ridge Regression   | 0.3423  |   -    |    -     |
| Lasso Regression   | 0.3557  |   -    |    -     |

- **Best Performing Model**: Linear Regression with all features
- **Best Simple Model**: Ridge Regression with engineered features
- **Top Predictors**: `sqft_living`, `grade`, `zipcode`, `sqft_living15`

---

## 💡 Key Takeaways

- Log transformation normalized skewed `price` data and improved model accuracy.
- `sqft_living`, `grade`, and `zipcode` were the most influential features.
- Ridge performed better than Lasso due to multicollinearity control.
- Model 2 improved slightly over Model 1 with the addition of `sqft_living15`.

---

## 📚 Technologies Used

- Python  
- Pandas, NumPy  
- Scikit-learn  
- Seaborn & Matplotlib  
- Jupyter/Colab Notebook  

---

## 🚀 How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/housing-price-prediction.git
   cd housing-price-prediction
   ```

2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

3. Launch the notebook:
   ```bash
   jupyter notebook
   ```

---

## 📌 Future Improvements

- Add Random Forest, XGBoost, SVR for comparison
- Feature selection with Recursive Feature Elimination (RFE)
- Deploy as an API with Flask/FastAPI
- Add interactive dashboard with Streamlit or Dash

---

## 📬 Contact

Feel free to reach out for questions or collaborations:

- 📧 Email: abdulrafaymohammed365@gmail.com
- 🧑‍💻 LinkedIn: [Abdul Rafay]([https://linkedin.com/in/your-profile](https://www.linkedin.com/in/abdulrafaymohammed365/))
