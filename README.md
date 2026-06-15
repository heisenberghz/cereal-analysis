
# Cereal Rating Analysis and Prediction
A data analysis and machine learning project that explores how nutritional attributes influence cereal ratings and uses Linear Regression to predict ratings from key nutrients.

## Overview

This project explores the nutritional characteristics of breakfast cereals and investigates how different nutrients influence consumer ratings. The analysis includes exploratory data analysis (EDA), correlation analysis, visualization, and a predictive model using Linear Regression.

## Files

- `cerealratings_analysis.ipynb` — analysis notebook
- `cereal.csv` — dataset used by the notebook
- `requirements.txt` — Python dependencies
- `.gitignore` — files and folders to exclude from Git
- `.gitattributes` — notebook diff settings for GitHub
- `LICENSE` — project license (MIT)

## Quickstart

1. Create and activate a virtual environment (recommended):

```bash
python -m venv .venv
source .venv/bin/activate   # macOS / Linux
.venv\Scripts\Activate.ps1 # Windows PowerShell
```

2. Install dependencies:

```bash
pip install -r requirements.txt
```

3. Open the notebook:

```bash
jupyter notebook cerealratings_analysis.ipynb
# or
jupyter lab cerealratings_analysis.ipynb
```

## Dataset

The dataset contains nutritional information for various breakfast cereals, including calories, protein, fat, sodium, fiber, carbohydrates, sugars, potassium, vitamins, and a consumer `rating`. Each row represents a cereal product.

## Project Workflow

1. Data exploration and cleaning (handle missing values and outliers).
2. Visualization of distributions and relationships between nutrients and ratings.
3. Correlation analysis to identify features related to `rating`.
4. Predictive modeling using Linear Regression (and brief comparison with Random Forest).

## Features used for the final model

- `protein`
- `fat`
- `sugars`

Target: `rating`.

Train/Test split: 70%/30% (random_state=109).

## Model results (summary)

- Linear Regression R²: 0.79996 (~80% explained variance)

Learned regression equation (rounded):

Rating = 43.23 + 6.78 × Protein − 4.04 × Fat − 1.85 × Sugars

Coefficients:

- Protein: 6.775
- Fat: -4.037
- Sugars: -1.854
- Intercept: 43.227

A Random Forest Regressor was also evaluated and achieved a slightly lower R² (~0.76) on the same split.

## Interpretation

- Higher protein is associated with higher ratings.
- Higher fat and sugars are associated with lower ratings in this dataset.
- The linear model explains the majority of variation for the selected features, suggesting a largely linear relationship.

## Reproducibility & notes

- The notebook reads `cereal.csv` from the repository root — keep the file in place or update the path.
- Consider clearing outputs from the notebook before committing to keep the repository lightweight.

## Future improvements

- Add additional features (fiber, sodium, potassium).
- Apply feature engineering and scaling where appropriate.
- Use cross-validation and hyperparameter tuning.
- Evaluate additional regression algorithms and compare using consistent metrics.

