# House Price Prediction — Short Project Report

## Objective

This project uses supervised regression to estimate house price per unit area from transaction date, house age, distance to the nearest MRT station, number of nearby convenience stores, latitude, and longitude. It uses the UCI Real Estate Valuation dataset (dataset ID 477).

## Models and evaluation

The notebooks compare ordinary Linear Regression with Ridge Regression (alpha = 1.0). Both models use median imputation and standardization inside a scikit-learn pipeline, and are trained using the same reproducible 70/30 train/test split (random seed 4775). The held-out test set is evaluated with mean absolute error (MAE), root mean squared error (RMSE), and R². Five-fold shuffled cross-validation provides an additional estimate of performance variability.

## Results

The repository contains runnable notebooks, but they have not been executed in this environment. Therefore, no numeric metrics or winning model are claimed here. Run all cells in [`linear_vs_ridge_comparison.ipynb`](linear_vs_ridge_comparison.ipynb) to generate the test-set comparison table, actual-versus-predicted plot, residual plot, and cross-validation results. Copy those observed results into the table below to complete the report.

| Model | Test MAE | Test RMSE | Test R² | Mean five-fold CV R² ± SD |
| --- | ---: | ---: | ---: | ---: |
| Linear Regression | Fill from notebook output | Fill from notebook output | Fill from notebook output | Fill from notebook output |
| Ridge Regression (alpha = 1.0) | Fill from notebook output | Fill from notebook output | Fill from notebook output | Fill from notebook output |

When interpreting the results, lower MAE/RMSE indicate smaller errors and higher R² indicates a closer fit. Compare the cross-validation mean and spread as well as the single test split; avoid treating a small difference as conclusive.

## Limitations

- The target is price per unit area in the dataset's original units, not a total home price.
- The dataset is historical and limited in scope; it may not represent present-day housing markets or other regions.
- A test score is not a guarantee of prediction accuracy for a new property. Predictions should not be used as professional valuation or financial advice.
- Ridge's alpha is fixed for demonstration and has not been tuned using nested validation.

## Reproducibility

Install the dependencies listed in the repository README and run the notebooks from top to bottom. Dataset retrieval requires internet access. The fixed random seed makes the split and folds reproducible, subject to dataset and library version stability.
