# INST346 — Sprint 3: Sanctuary Policy & Unemployment Modeling
This repository contains all Sprint 3 deliverables for analyzing how sanctuary status, poverty rates, and hate-crime rates predict unemployment across U.S. cities. The repo includes modeling scripts, results, figures, and saved model artifacts, along with reproducible notebooks and clear documentation.

Sprint 3 focused on building, tuning, and evaluating supervised regression models to understand and predict unemployment levels across U.S. cities. Two models were implemented:

1. Linear Regression (interpretable baseline model)

2. Random Forest Regression (nonlinear predictive model)

Key Sprint 3 achievements include:

- Full preprocessing pipeline (cleaning, log transformations, interaction terms)

- Baseline, Linear Regression, and Random Forest models trained and compared

- Hyperparameter tuning via 5-fold cross-validation

- Residual diagnostics, error analysis, and feature importance evaluation

- Saved models and visualizations for reproducibility

- Repository organized for Sprint 4 continuation

The Random Forest model demonstrated the strongest performance, capturing nonlinear relationships and reducing error across cities. Linear Regression remained valuable for policy interpretation.

Repository structure: 
INST346-Sprint3/
│
├── data/
│   ├── raw/                # original dataset(s)
│   └── processed/          # cleaned, transformed dataset
│
├── notebooks/
│   └── sprint3-modeling.ipynb    # full modeling workflow
│
├── scripts/
│   ├── preprocess.py              # cleaning + transformation steps
│   ├── baseline.py                # mean baseline model
│   ├── linear_regression.py       # linear model training + evaluation
│   └── random_forest.py           # RF model training + evaluation
│
├── models/
│   ├── rf_model.pkl               # trained Random Forest artifact
│   ├── lr_model.pkl               # trained Linear Regression artifact
│   └── model_params.json          # tuned hyperparameters
│
├── results/
│   ├── metrics.csv                # MAE/RMSE/R² results
│   ├── evaluation_summary.md      # written interpretation
│   └── error_tables.csv           # high/low error cases (optional)
│
├── figures/
│   ├── feature_importance.png
│   ├── residual_plot_lr.png
│   ├── predictions_vs_actual.png
│   └── error_distribution.png
│
└── README.md                      # project documentation (this file)


Modeling Workflow Overview
1. Preprocessing

Load raw dataset

Handle missing values

Create new engineered features

Apply log-transform to skewed variables (hate crime rate)

Standardize predictors for Linear Regression

Save processed dataset to /data/processed/

2. Baseline Model

Predicts the mean unemployment rate for every city.
Used as the minimum performance benchmark.

3. Linear Regression Model

Uses sanctuary status, poverty rate, log(hate crime rate), and interactions

Produces interpretable coefficients

Sensitive to nonlinear relationships

Improves on the baseline

Saved as lr_model.pkl

4. Random Forest Regression

Captures nonlinear interactions

Robust to outliers

Highest R² and lowest MAE/RMSE

Feature importance identifies strongest predictors

Saved as rf_model.pkl

5. Evaluation & Diagnostics

Includes:

5-fold cross-validation

Residual analysis

Error distribution plots

Predicted vs. actual diagrams

High-error case analysis

All results are stored in /results/ and /figures/.

How to run: 
To run this project, start by opening the repository on your computer and making sure you have Python installed. Then install the required packages using the requirements.txt file. After that, you can run the scripts in the scripts folder to clean the data and train the models. The main Jupyter Notebook in the notebooks folder can also be opened to see the full workflow, including data loading, model training, and evaluation. All results, such as metrics and charts, will be saved automatically into the results and figures folders. The saved models can be found inside the models folder. Following these steps will let you run the project and see the same results shown in Sprint 3.
