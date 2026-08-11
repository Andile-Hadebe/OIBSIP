# 🏠 House Price Prediction with Linear Regression

## 📊 Project Overview

This project predicts house prices using Linear Regression based on property features like area, bedrooms, location, and condition. Part of my Data Analytics internship at **Oasis Infobyte**.

## 🎯 Objectives

- Clean and preprocess housing data
- Engineer new features (Age from YearBuilt)
- One-hot encode categorical variables
- Build and evaluate Linear Regression models
- Identify key drivers of house prices
- Compare Ridge and Lasso regularization

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python | Core language |
| pandas | Data manipulation |
| numpy | Numerical operations |
| matplotlib | Static visualizations |
| seaborn | Statistical visualizations |
| scikit-learn | Modeling & evaluation |

## 📈 Key Findings

| Feature | Coefficient | Interpretation |
|---------|-------------|----------------|
| **Condition_Fair** | +24,083 | Fair condition homes tend to be priced higher |
| **Floors** | +23,728 | Each additional floor adds ~R23,700 to price |
| **Location_Suburban** | +11,512 | Suburban locations add ~R11,500 to price |
| **Age** | -118 | Each additional year reduces price by ~R118 |
| **Location_Urban** | -12,719 | Urban locations show a slight negative impact |

## ⚠️ Critical Lessons Learned

### 🔥 Data Leakage
- The `Id` column was used as a feature — the model learned from the ID, not property features
- **Fix:** Removed `Id` from feature set

### 🔥 Scaling Before Splitting
- Scaling was applied before train-test split — leaking test data into training
- **Fix:** Scale after splitting the data

### 🔥 Wrong R² Argument Order
- `r2_score(y_pred, y_test)` vs correct `r2_score(y_test, y_pred)`
- **Fix:** Corrected the order

## 📊 Model Performance (After Fixes)

| Model | R² Score |
|-------|----------|
| **Linear Regression** | -0.0067 |
| **Ridge (α=1.0)** | -0.0067 |
| **Lasso (α=0.01)** | -0.0067 |

## 🚀 How to Run

1. Clone this repository
2. Ensure Python 3.x is installed
3. Install dependencies: `pip install pandas numpy matplotlib seaborn scikit-learn`
4. Open the Jupyter Notebook
5. Run all cells

## 📬 Connect

- **Author:** Andile Hadebe
- **Email:** andilesbuyis@gmail.com
- **LinkedIn:** https://www.linkedin.com/in/andile-hadebe

---

**Made with ❤️ by Andile Hadebe**
