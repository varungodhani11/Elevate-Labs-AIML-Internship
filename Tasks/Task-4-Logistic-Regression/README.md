# Task 4 - Logistic Regression

## Objective

Implement a Logistic Regression model for binary classification, evaluate its performance using classification metrics, tune the classification threshold, and understand the sigmoid function.

## Dataset

The project uses the Breast Cancer Wisconsin dataset provided as `data.csv`.

- Rows: 569
- Original columns: 33
- Target column: `diagnosis`
- `B` = Benign
- `M` = Malignant

During preprocessing:
- `id` was removed because it is an identifier.
- `Unnamed: 32` was removed because it contains only missing values.
- `diagnosis` was encoded as `0` and `1`.
- The resulting dataset contains 30 numerical predictor features.
- No duplicate rows were found.

## Methodology

1. Loaded and inspected the dataset.
2. Removed the identifier and empty column.
3. Encoded the binary target variable (`B` = 0, `M` = 1).
4. Separated the data into features (`X`) and target (`y`).
5. Split the data into training and testing sets using an 80:20 split with stratification and `random_state=42`.
6. Standardized features using `StandardScaler`, fitting the scaler only on the training data to avoid data leakage.
7. Trained a `LogisticRegression` model.
8. Generated class predictions and malignant-class probabilities.
9. Evaluated the model using a confusion matrix, precision, recall, and ROC-AUC.
10. Plotted the ROC curve.
11. Tested multiple classification thresholds and selected `0.3` as the tuned threshold.
12. Explained and visualized the sigmoid function.

## Model Performance

### Default Threshold: 0.5

| Metric | Result |
|---|---:|
| Precision | 97.50% |
| Recall | 92.86% |
| ROC-AUC | 99.60% |

Confusion Matrix:

```text
[[71,  1],
 [ 3, 39]]
```

### Tuned Threshold: 0.3

| Metric | Result |
|---|---:|
| Precision | 97.62% |
| Recall | 97.62% |

Tuned Confusion Matrix:

```text
[[71,  1],
 [ 1, 41]]
```

Lowering the threshold from `0.5` to `0.3` increased recall from `92.86%` to `97.62%`, while precision remained very high.

## Sigmoid Function

Logistic Regression uses the sigmoid function to convert the model's linear output into a probability between 0 and 1:

```text
sigmoid(z) = 1 / (1 + e^(-z))
```

The notebook includes a sigmoid visualization showing the relationship between the linear model output and probability. The default classification threshold of `0.5` corresponds to a sigmoid output of 0.5. The project separately tunes the classification threshold to `0.3`.

## Tools and Libraries

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook

## Repository Contents

- `Task_4_Logistic_Regression.ipynb` - Complete implementation and analysis
- `data.csv` - Dataset used for the project
- `README.md` - Project documentation

## Conclusion

The Logistic Regression model achieved a ROC-AUC of `0.9960` on the test set. Threshold tuning from `0.5` to `0.3` improved recall to `97.62%` while maintaining precision at `97.62%`.

This project demonstrates the workflow of preprocessing data, training a Logistic Regression classifier, evaluating classification performance, tuning the decision threshold, and understanding the sigmoid function.
