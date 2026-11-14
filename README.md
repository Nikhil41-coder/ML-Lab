<h1 align="center">🤖 Machine Learning Laboratory</h1>

<p align="center">
  <b>5th Semester · Academic Year 2026–27</b><br>
  <i>Hands-on implementations of core supervised-learning algorithms in Python</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white" />
  <img src="https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white" />
  <img src="https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white" />
  <img src="https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white" />
</p>

---

## 📌 About

This repository has my Machine Learning Lab work. Each notebook covers one concept, from fitting a straight line to regularized regression, and shows **how the model is built** and **how it's evaluated**. Several experiments compute the results by hand (normal equations, a closed-form Lasso) alongside scikit-learn, so the maths behind each model is visible.

---

## 🗂️ Experiments at a Glance

| # | Experiment | Concept | Notebook |
|:-:|------------|---------|----------|
| 1 | Simple Linear Regression | Regression · R² · MSE | [`experiment_1_linear-regression.ipynb`](experiment_1_linear-regression.ipynb) |
| 2 | K-Fold Cross Validation | Model validation | [`experiment_2_kfold.ipynb`](experiment_2_kfold.ipynb) |
| 3 | Degree-2 Polynomial Regression | Normal equations | [`experiment_3_2degree_poly.ipynb`](experiment_3_2degree_poly.ipynb) |
| 4 | Regularization: OLS vs Ridge vs Lasso | L1 / L2 penalties | [`experiment_4_regularization_lasso_ridge.ipynb`](experiment_4_regularization_lasso_ridge.ipynb) |
| A1 | Activity 1: Regression & Regularization | Train / validation / test | [`activity_1.ipynb`](activity_1.ipynb) |

---

## 🔬 Experiment Details

### 🔹 Experiment 1: Simple Linear Regression
Predicts **Marks** from **Hours Studied**.
- Load the dataset with Pandas
- Fit `LinearRegression` and get the **slope** and **intercept**
- Predict marks for every student
- Evaluate with **R² score** and **Mean Squared Error**
- Plot the actual data against the regression line
- Predict the marks for a new input (10 hours of study)

📄 *Dataset:* `linear_regression.csv`

### 🔹 Experiment 2: K-Fold Cross Validation
Checks how well Linear Regression generalizes beyond a single split.
- Split the data into **5 folds** with `KFold`
- In each fold, train on 4 parts and test on the remaining 1
- Report the per-fold coefficients, **MSE** and **R²**

📄 *Dataset:* `k_fold_linear_regression (2).csv`

### 🔹 Experiment 3: Second-Degree Polynomial Regression
Fits **y = ax² + bx + c** from first principles, without a model library.
- Build the design matrix `[x², x, 1]`
- Compute **XᵀX** and **Xᵀy**
- Solve the **normal equation** β = (XᵀX)⁻¹Xᵀy to get *a*, *b* and *c*
- Compute the **MSE** and **R²** manually
- Plot the fitted parabola against the data points

📄 *Dataset:* `Degree 2 Polynomial.csv`

### 🔹 Experiment 4: Regularization (OLS vs Ridge vs Lasso)
Compares ordinary least squares with its regularized versions on a linear dataset (x = 1…9).
- **Split:** train (x = 1–5) · validation (x = 6–7) · test (x = 8–9)
- **OLS:** `LinearRegression`
- **Ridge (L2):** `Ridge(alpha=1)`
- **Lasso (L1):** a closed-form soft-thresholding solution, `m = sign(m_ols)·max(0, |m_ols| − 1/S)`
- Prints each model's equation and predictions, and summarizes the **Train / Validation / Test MSE** in one table

📄 *Dataset:* defined inside the notebook

### 🔹 Activity 1: Regression & Regularization
A hands-on activity that repeats the OLS → Ridge → Lasso workflow with the same three-way split and puts the results side by side in a single comparison table.

📄 *Dataset:* defined inside the notebook

---

## 📊 Evaluation Metrics Used

| Metric | What it tells us |
|--------|------------------|
| **MSE** | Average squared error between prediction and truth (lower is better) |
| **R² Score** | Share of the variance in the target that the model explains (closer to 1 is better) |
| **Train vs Validation vs Test MSE** | Whether a model is underfitting, overfitting or generalizing well |

---

## ⚙️ Getting Started

```bash
# 1. Clone the repository
git clone <your-repo-url>
cd <repo-folder>

# 2. Install dependencies
pip install numpy pandas matplotlib scikit-learn jupyter

# 3. Launch Jupyter
jupyter notebook
```

> 💡 All datasets are included in this repository. On Google Colab, upload the CSV for the experiment along with the notebook before running the cells.

---

## 📁 Repository Structure

```
.
├── experiment_1_linear-regression.ipynb          # Simple Linear Regression
├── experiment_2_kfold.ipynb                      # K-Fold Cross Validation
├── experiment_3_2degree_poly.ipynb               # Polynomial Regression (normal equation)
├── experiment_4_regularization_lasso_ridge.ipynb # OLS vs Ridge vs Lasso
├── activity_1.ipynb                              # Regression & Regularization activity
├── linear_regression.csv                         # Dataset for Experiment 1
├── k_fold_linear_regression (2).csv              # Dataset for Experiment 2
├── Degree 2 Polynomial.csv                       # Dataset for Experiment 3
└── README.md
```

---

## 🎯 Learning Outcomes

- Build and interpret a linear regression model (slope, intercept, R²)
- Understand why **cross-validation** gives a more reliable estimate than one split
- Derive polynomial regression coefficients from the **normal equation**
- See how **L2 (Ridge)** shrinks coefficients and **L1 (Lasso)** can push them to zero
- Use train / validation / test splits to diagnose **underfitting and overfitting**

---

<p align="center">
  <b>👨‍💻 Nikhil</b><br>
  USN: 4NI24CI070<br>
  CSE (AI & ML) · The National Institute of Engineering, Mysuru<br>
  <i>Machine Learning Laboratory · 2026–27</i>
</p>

<p align="center">⭐ <b>LEARN · IMPLEMENT · EXPERIMENT</b> ⭐</p>
