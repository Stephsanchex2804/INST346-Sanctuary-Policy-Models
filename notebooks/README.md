



## 📊 Sprint 3 – Modeling & Evaluation (ADSP)

This sprint focuses on building, evaluating, and comparing predictive models for unemployment outcomes using county-level immigration and demographic data.


---

### 📓 Main Notebook
  

➡️ **`03_sprint3_modeling.ipynb`**  
`notebooks/03_sprint3_modeling.ipynb`

---

### ⚙️ How to Run
or manually:



Then:

1. Clone the repository
2. Open `03_sprint3_modeling.ipynb`
3. Run all cells (top → bottom)

---

### 🧠 Models Trained
- Baseline (DummyRegressor)
- Linear Regression
- Random Forest Regressor
**Note:** The full Random Forest model had a large file size and exceeded GitHub’s upload limit (100MB). Therefore, only the baseline and linear regression artifacts are included in the `models/` folder. The Random Forest model can be re-created directly from the notebook using the same training code.

---

### 🗂 Saved Outputs

#### 📁 `models/`
- baseline_dummy_regressor.joblib
- linear_regression.joblib
- random_forest_regressor.joblib

#### 📁 `results/`
- model_comparison_metrics.csv

#### 📁 `figures/`
- rf_feature_importance_top10.png
- rf_actual_vs_predicted.png

---

### 🏁 Status
✔ Sprint 3 technical implementation completed  
✔ Models saved  
✔ Results saved  
✔ Figures generated

Writing/analysis interpretation coming next in Sprint 3 report.

