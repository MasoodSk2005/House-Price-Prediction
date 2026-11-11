### House Price Prediction

A machine learning project that predicts median house values using Scikit-Learn pipelines, cross-validation, and hyperparameter tuning.

---

## Project Workflow

1. **Exploratory Data Analysis (EDA):**
   * Checked shape, data types, missing values, and duplicate rows.
   * Visualized target distribution, numerical feature distributions, categorical distributions, and feature correlations.
2. **Data Preprocessing & Pipelines:**
   * Built automated pipelines using `ColumnTransformer` and `Pipeline`.
   * **Numerical Features:** Imputed missing values with median strategy and scaled with `StandardScaler`.
   * **Categorical Features:** Imputed missing values with most frequent strategy and encoded with `OneHotEncoder(handle_unknown="ignore")`.
3. **Model Evaluation & Cross-Validation:**
   * Split dataset (80% train, 20% test, `random_state=42`).
   * Evaluated multiple regression models using 5-fold cross-validation evaluated on RMSE, MAE, and $R^2$.
4. **Hyperparameter Tuning:**
   * Optimized the top model using `GridSearchCV`.
5. **Evaluation & Inference:**
   * Analyzed residual distribution and created a custom prediction function for single sample inference.

---

## Algorithms Evaluated

* Linear Regression (Baseline)
* Ridge Regression
* Lasso Regression
* Random Forest Regressor
* **HistGradientBoostingRegressor** *(Selected as final tuned model)*

---

## How to Run Locally

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/house-price-prediction.git
cd house-price-prediction
```

### 2. Add Dataset
Ensure `housing.csv` is placed in the project root directory alongside `House_Price_Prediction.ipynb`.

### 3. Run the Notebook
Launch Jupyter and run `House_Price_Prediction.ipynb` notebook's all cells

---
