# Task 2: Exploratory Data Analysis

## Objective
Understand a dataset through summary statistics and visualizations, and identify patterns, trends, and anomalies.

## Dataset
`cleaned_ecommerce_customer_churn.csv` - the cleaned, unscaled E-commerce Customer Churn dataset produced by Task 1 (3,267 rows, 15 columns, no missing values, no duplicates). This notebook does not repeat any cleaning; it loads the dataset exactly as Task 1 saved it.

## Analysis Performed
- Loaded the cleaned dataset and checked shape, data types, missing values, and duplicates as a basic validation.
- Generated summary statistics for the numerical features.
- Plotted histograms and boxplots for the numerical features.
- Reconstructed and plotted categorical distributions (`PreferedOrderCat`, `MaritalStatus`) from the one-hot encoded columns produced in Task 1.
- Looked at the `Churn` (target) distribution - about 16% of customers churned.
- Built a correlation matrix and heatmap for the numerical features and `Complain` against `Churn`.
- Compared churn rate across groups: `Complain`, preferred order category, and marital status, plus tenure differences between churned and retained customers.
- Built a pairplot on a small, deliberately chosen subset of numerical features, colored by churn.
- Wrote up patterns and feature-level inferences based only on the actual outputs generated in the notebook.

## Tools Used
Python, Pandas, NumPy, Matplotlib, Seaborn, Plotly

## Key Findings
Customers with lower tenure show a much higher observed churn rate (median tenure 1 vs 9) - the strongest single pattern found (correlation -0.34). Customers who filed a complaint churn at roughly 3x the rate of those who didn't (~32% vs ~10%), and customers whose preferred order category is "Mobile" churn more often (~27%) than most other categories. These are observed associations in this dataset, not proof of causation.

## How to Run
1. Make sure `cleaned_ecommerce_customer_churn.csv` is in the same folder as the notebook.
2. Open `Task_2_Exploratory_Data_Analysis.ipynb` in Jupyter.
3. Run all cells top to bottom (Run All). No manual steps or out-of-order execution needed.
