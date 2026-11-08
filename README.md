# Machine Learning Exercises

This repository contains machine-learning practice notebooks, starting with a house-price prediction project using the UCI Real Estate Valuation dataset.

## Contents

- [`house_price_prediction.ipynb`](house_price_prediction.ipynb) — data exploration, model evaluation, visualizations, cross-validation, and an example prediction.
- [`linear_vs_ridge_comparison.ipynb`](linear_vs_ridge_comparison.ipynb) — focused comparison of Linear Regression and Ridge Regression on the same train/test split, including metrics and diagnostic plots.
- [`HOUSE_PRICE_REPORT.md`](HOUSE_PRICE_REPORT.md) — a concise project report and guidance for adding results produced by running the comparison notebook.

## Run the notebooks

1. Clone or download this repository.
2. Open a terminal in the project folder and install dependencies:

   ```bash
   python -m pip install ucimlrepo pandas numpy matplotlib seaborn scikit-learn jupyter
   ```

3. Start Jupyter:

   ```bash
   jupyter notebook
   ```

4. Open a notebook and run its cells from top to bottom. In Google Colab, open the notebook from GitHub and run the dependency-install cell first.

The notebooks fetch UCI dataset 477 over the internet, so network access is required the first time the dataset is loaded.

## Dataset and target

The project uses the [UCI Real Estate Valuation dataset](https://archive.ics.uci.edu/dataset/477/real+estate+valuation+data+set). The target is **house price per unit area** in the source dataset's original units—not a home's total sale price. The dataset is historical and should be treated as an educational example, not current market guidance.

## Modeling notes

The notebooks use a held-out test set for evaluation and put median imputation and feature standardization inside scikit-learn pipelines. This ensures preprocessing is fit only on training data (and, during cross-validation, only on each training fold). The comparison notebook reports MAE, RMSE, and R² and computes five-fold cross-validation scores.

## Reproducibility

A fixed random seed is used for the train/test split and shuffled cross-validation. Dataset availability, library versions, and upstream data changes may still affect results.
