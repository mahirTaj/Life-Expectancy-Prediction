# 🌍 Life Expectancy Prediction (WHO)

A machine learning project that predicts life expectancy across different countries using health, economic, and social factors. The project leverages WHO and UN datasets and compares multiple ML models to determine the most effective predictor.

---

## 📌 Project Overview

* **Course**: CSE422 – Artificial Intelligence
* **Topic**: Life Expectancy Prediction
* **Dataset Source**: [WHO Life Expectancy Dataset](https://www.kaggle.com/datasets/kumarajarshi/life-expectancy-who)
* **Type**: Regression (predicting continuous values)
* **Group**: 10, Section 03

---

## 📊 Dataset

* **Rows**: 2938
* **Columns**: 22 (21 features + 1 target)
* **Features**:

  * Quantitative: GDP, Adult Mortality, Immunization rates, etc.
  * Categorical: Country, Status (Developed/Developing)
* **Target**: Life Expectancy (in years)

---

## 🛠️ Preprocessing

* **Null values**: Filled using **KNN imputer**
* **Outlier treatment**: Used whisker method with capping
* **Encoding**: One-hot encoding for categorical variables (Country, Status)
* **Feature selection**: Dropped highly correlated features (>75%)
* **Scaling**: Min-Max normalization applied to all features

---

## 🔀 Dataset Splitting

* **Train**: 70%
* **Test**: 30%

---

## 🤖 Models Implemented

1. **Linear Regression**

   * Achieved best performance overall
   * Metrics: MAE, MSE, RMSE, R²

2. **Decision Tree Regressor**

   * Higher error rates than Linear Regression
   * Useful for non-linear relationships but less efficient here

3. **Neural Network**

   * Architecture: 3 layers (64 → 32 → 1 neuron)
   * Optimizer: Adam
   * Loss: Mean Squared Error
   * Trained for 100 epochs

---

## 📈 Results & Comparison

* **Linear Regression**:

  * Best performer with lowest MAE, MSE, RMSE
  * Highest R² value
  * Simple, efficient, and interpretable

* **Decision Tree**:

  * Higher errors, not optimal for this dataset

* **Neural Network**:

  * Competitive results but required more resources
  * Slightly higher error than Linear Regression

📌 **Final Model Choice**: **Linear Regression** (best trade-off between performance and simplicity)

---

## ✅ Conclusion

* Life expectancy is influenced by multiple health, social, and economic factors.
* Linear Regression proved to be the most practical model for this dataset.
* Neural Networks can be used but require higher computation with no significant performance gain.
* Decision Trees were less effective in this case.

---

## 🚀 Future Work

* Try **ensemble methods** (Random Forest, XGBoost)
* Use **deep learning with embeddings** for categorical features
* Apply **feature engineering** to improve interpretability
* Explore **global health policy implications** based on predictions

---

## 📖 License

This project is open-source and available under the [MIT License](LICENSE).
