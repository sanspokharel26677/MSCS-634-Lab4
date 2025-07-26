# MSCS-634

# Lab 4: Regression Analysis with Regularization Techniques

**Course:** Advanced Big Data and Data Mining (MSCS-634-B01)  
**Author:** Sandesh Pokharel  

---

## 📌 Purpose of the Lab

The purpose of this lab was to explore multiple regression techniques and understand how regularization can improve model performance. Using the **Diabetes dataset** from `sklearn.datasets`, we implemented and compared:
- Simple Linear Regression  
- Multiple Linear Regression  
- Polynomial Regression (degree 2)  
- Ridge Regression  
- Lasso Regression  

The lab also aimed to visualize model predictions, evaluate using standard metrics, and understand the impact of regularization parameters (`alpha`) on model performance.

---

## 🔑 Key Insights from the Regression Analysis

1. **Simple Linear Regression** (BMI as the only feature) performed the worst with R² = 0.23, showing that using a single feature is not sufficient for accurate predictions.  
2. **Multiple Linear Regression** improved R² to 0.45 by using all features, but still suffered from moderate bias and variance.  
3. **Polynomial Regression (degree 2)** added complexity but did not significantly outperform Multiple Regression, suggesting the relationships were largely linear.  
4. **Regularized Models (Ridge & Lasso):**
   - Both models reduced overfitting when the right `alpha` was chosen.
   - **Lasso Regression (alpha = 0.1)** achieved the best performance overall with R² = **0.472** and the lowest RMSE = **52.9**.
   - Lasso also helps with feature selection by setting less relevant coefficients to zero, improving model interpretability.

5. Choosing the correct `alpha` is critical:
   - Too low → risk of overfitting.  
   - Too high → underfitting (R² dropped significantly at alpha = 10).  

---

## ⚠️ Challenges and Decisions

- **Choosing the right feature for Simple Linear Regression:** We selected **BMI** because it had the highest correlation with the target variable.  
- **Balancing polynomial degree:** Degree 2 was chosen to avoid overfitting and excessive complexity.  
- **Alpha tuning:** We tested multiple alpha values (0.1, 1.0, 10.0) and observed their impact on Ridge and Lasso. We selected **alpha = 0.1** as the best performing regularization strength.  
- **Interpretation of metrics:** While R² provides a good measure of explained variance, we also relied on RMSE and MAE to capture error magnitudes.  

---

## 📊 Dataset Information

- **Dataset:** Diabetes dataset (`sklearn.datasets.load_diabetes()`)
- **Rows:** 442  
- **Features:** 10 baseline variables (age, sex, BMI, blood pressure, and 6 blood serum measurements)  
- **Target:** Disease progression after one year (continuous)

---

## 🧰 Tools and Libraries Used

- **Python 3.13**
- **Jupyter Notebook**
- **Libraries:** `numpy`, `pandas`, `scikit-learn`, `matplotlib`, `seaborn`

---

## 🚀 Key Takeaways

- Regularization is critical to balance bias-variance and improve model generalization.
- Lasso is particularly useful when feature selection and interpretability are priorities.
- Cross-validation should be used in production to fine-tune hyperparameters like `alpha`.

---

## 📂 Repository Structure
MSCS-634-Lab4/
├── MSCS-634-Lab4.ipynb     # Jupyter Notebook with all steps, code, and explanations
├── README.md               # Project documentation
└── MSCS-643_Lab4_Instructions.pdf  # Assignment instructions

---

## ✨ Author

Sandesh Pokharel  
