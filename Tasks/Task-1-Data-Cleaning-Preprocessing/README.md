# Task 1: Data Cleaning & Preprocessing

## Objective
Clean and preprocess a raw dataset so it is ready for modeling - handle missing values, encode categorical features, treat outliers, and standardize numerical features.

## Dataset
E-commerce Customer Churn dataset (`data_ecommerce_customer_churn.csv`), 3,941 rows and 11 columns before cleaning.

## Work Done
- Explored the dataset (shape, data types, missing values, summary statistics).
- Found and removed 671 exact duplicate rows before doing anything else with the data.
- Found missing values in `Tenure`, `WarehouseToHome`, and `DaySinceLastOrder`. All three are right-skewed, so filled them with the column median.
- Found that `PreferedOrderCat` had `Mobile` and `Mobile Phone` listed as two separate categories for what is really the same category, and merged them before encoding.
- One-hot encoded the remaining categorical columns (`PreferedOrderCat`, `MaritalStatus`).
- Visualized the numerical features with boxplots (on unscaled data) and used the 1.5 x IQR rule to flag potential outliers.
- Checked the actual flagged values for every column before deciding what to do, instead of removing everything IQR flagged. Only `WarehouseToHome = 127` was removed - a single value far outside the normal 5-36 range with no realistic explanation, removed using a condition on the IQR bound rather than a hardcoded row index.
- Ran a final duplicate check before finalizing the cleaned dataset, since imputation and category merging can occasionally make two originally different rows identical.
- Saved the cleaned dataset in its original, unscaled units (`cleaned_ecommerce_customer_churn.csv`) - this is what Task 2 uses for its EDA.
- Standardized the numerical features with `StandardScaler` on a separate copy, applied only after all the cleaning steps above, and saved that version separately (`cleaned_ecommerce_customer_churn_scaled.csv`).

## Tools Used
Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn (StandardScaler)

## Output
- `cleaned_ecommerce_customer_churn.csv` - cleaned, unscaled dataset: **3,267 rows x 15 columns**, no missing values, no duplicate rows, fully numeric. Used directly by Task 2.
- `cleaned_ecommerce_customer_churn_scaled.csv` - same dataset with the numerical features standardized (mean ~0, std ~1). `Churn` is not scaled in either file.

## How to Run
1. Make sure `data_ecommerce_customer_churn.csv` is in the same folder as the notebook.
2. Open `Task_1_Data_Cleaning_Preprocessing.ipynb` in Jupyter.
3. Run all cells top to bottom (Run All). No manual steps or out-of-order execution needed.
