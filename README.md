# 🏡 Robust Regression Engine

A complete Machine Learning project for **House Price Prediction** using Regularized Linear Models, Cross-Validation Strategies, Tree-Based Regressors, and Support Vector Regression.

---

# 📌 Project Objective

The objective of this project is to:

- Build a robust regression pipeline for house price prediction.
- Reduce overfitting using regularization techniques.
- Compare linear and non-linear regression models.
- Apply multiple cross-validation strategies.
- Select the best-performing model.
- Evaluate model generalization on unseen data.

---

# 📂 Dataset Overview

The dataset contains real-estate property information such as:

- Property Size (area_sqft)
- Bedrooms
- Bathrooms
- Location Score
- Property Age
- Distance from City
- Crime Rate Index
- Near School
- Near Metro
- Sale Date
- House Price (Target Variable)

---

# 🛠️ Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-Learn
- Jupyter Notebook

---

# 📁 Project Structure

```text
Robust-Regression-Engine/
│
├── data/
│   └── house price.csv
│
├── notebooks/
│   └── rre.ipynb
│
├── outputs/
│   ├── plots/
│   ├── models/
│   └── reports/
│
├── README.md
├── requirements.txt
└── report.pdf
```

---

# 🔍 Exploratory Data Analysis

Performed:

- Dataset Shape & Information
- Missing Value Analysis
- Duplicate Value Analysis
- Distribution Analysis
- Correlation Heatmap
- Pairplots
- Feature vs Target Relationships
- Categorical Feature Analysis

### Key Findings

- Area has the strongest positive impact on house prices.
- Better location scores increase house value.
- Crime rate and distance from city negatively affect prices.
- Properties near schools and metro stations tend to be more expensive.

---

# ⚙️ Data Preprocessing

### Feature Engineering

Created:

- sale_year
- sale_month

### Data Cleaning

- Removed property_id
- Removed sale_date
- Outlier treatment using IQR Method

### Train-Test Split

- 80% Training Data
- 20% Testing Data

### Feature Scaling

Applied StandardScaler for:

- Ridge Regression
- Lasso Regression
- Support Vector Regression

---

# 📈 Regularized Linear Models

## Ridge Regression (L2)

Implemented:

- RidgeCV
- Alpha tuning using Cross Validation

### Result

- Better stability
- Reduced overfitting
- All coefficients retained

---

## Lasso Regression (L1)

Implemented:

- LassoCV
- Automatic alpha selection

### Result

- Performs feature selection
- Removes less important features
- Produces sparse coefficients

---

# 🔄 Cross Validation Strategies

Implemented:

### 1. K-Fold Cross Validation

- 5 Folds
- Shuffle Enabled

### 2. Stratified K-Fold

- Target variable binned into categories

### 3. Leave One Out Cross Validation (LOOCV)

- Applied on sample data

### 4. Time Series Split

- Based on sale_year

### Findings

- K-Fold and Stratified K-Fold produced stable results.
- Time Series Split showed higher variation.
- Useful for measuring model robustness.

---

# 🌳 Tree Based Models

## Decision Tree Regressor

### Default Tree

- Severe overfitting
- Training R² ≈ 1.0

### Controlled Tree

Hyperparameters:

- max_depth = 8
- min_samples_split = 20
- min_samples_leaf = 10

### Result

- Better generalization
- Reduced overfitting

---

## Random Forest Regressor

Hyperparameters:

- n_estimators = 100
- max_depth = 15
- min_samples_split = 10

### Result

✅ Best Performing Model

- Highest Test R²
- Lowest RMSE
- Strong generalization

---

# 🤖 Support Vector Regression

## Linear Kernel

- C = 10
- epsilon = 0.1

## RBF Kernel

- C = 100
- gamma = 0.1
- epsilon = 0.1

### Findings

- Linear SVR performed slightly better.
- RBF kernel struggled to generalize on this dataset.

---

# 📊 Evaluation Metrics

Models evaluated using:

- Mean Squared Error (MSE)
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

---

# 🏆 Model Comparison

Models Compared:

1. Ridge Regression
2. Lasso Regression
3. Decision Tree Regressor
4. Random Forest Regressor
5. Linear SVR
6. RBF SVR

### Best Model

🥇 Random Forest Regression

Performance:

- Highest Test R² ≈ 0.93
- Lowest RMSE ≈ 2.06 Million

---

# 🚨 Overfitting & Underfitting Analysis

### Overfitting

Observed in:

- Default Decision Tree

Reason:

- Perfect training performance
- Lower testing performance

### Underfitting

Observed in:

- SVR Models

Reason:

- Low predictive power
- Weak test performance

### Balanced Models

- Random Forest
- Ridge Regression

---

# 📉 Residual Analysis

Residual plots show:

- Random scatter around zero
- No major prediction bias
- Near-normal residual distribution

This indicates that the Random Forest model generalizes well.

---

# 💼 Business Insights

- Property area is the strongest price driver.
- Better locations significantly increase value.
- Metro and school accessibility increase property prices.
- High crime rates negatively impact house values.
- Ensemble models are more suitable for real-estate price prediction.

---

# 🎯 Final Conclusion

After comparing all regression models:

✅ Random Forest Regression emerged as the best model.

Reasons:

- Highest predictive accuracy
- Lowest prediction error
- Strong generalization capability
- Less sensitive to outliers and feature scaling

The project successfully demonstrates how regularization, cross-validation, and ensemble learning can be used to build a robust house-price prediction system.

---

# 🚀 Installation

```bash
git clone https://github.com/your-username/Robust-Regression-Engine.git

cd Robust-Regression-Engine

pip install -r requirements.txt

jupyter notebook
```

---

# 📦 Requirements

```txt
numpy
pandas
matplotlib
seaborn
scikit-learn
jupyter
```

---

# 👨‍💻 Author

Machine Learning Project – Robust Regression Engine

Developed using Supervised Learning techniques for House Price Prediction.
