# Task 3: Linear Regression

## Objective

Implement and understand Simple Linear Regression and Multiple Linear Regression for predicting house prices.

## Dataset

The project uses the Housing Price Prediction dataset.

- Dataset file: `Housing.csv`
- Rows: 545
- Columns: 13
- Target variable: `price`

## Work Done

- Loaded and inspected the housing dataset.
- Checked data types, missing values, duplicate rows, and summary statistics.
- Converted categorical variables into numerical features using one-hot encoding.
- Split the data into training and testing sets using an 80:20 split.
- Built a Simple Linear Regression model using `area` as the predictor.
- Evaluated the simple model using MAE, MSE, and R².
- Built a Multiple Linear Regression model using the available features.
- Evaluated the multiple model using MAE, MSE, and R².
- Visualized the simple regression line.
- Compared actual and predicted house prices.
- Interpreted the regression coefficients.

## Model Performance

### Simple Linear Regression

- MAE: 1,474,748.13
- MSE: 3,675,286,604,768.19
- R²: 0.2729

### Multiple Linear Regression

- MAE: 970,043.40
- MSE: 1,754,318,687,330.66
- R²: 0.6529

The Multiple Linear Regression model performed better than the Simple Linear Regression model, with lower MAE and MSE and a higher R² score.

## Files

- `Task_3_Linear_Regression.ipynb` - Notebook containing the complete analysis and models.
- `Housing.csv` - Dataset used for the project.
- `README.md` - Project documentation.

## Conclusion

Using multiple house features provides better predictive performance than using area alone. The Multiple Linear Regression model achieved an R² of 0.6529 on the test data, compared with 0.2729 for the Simple Linear Regression model.
