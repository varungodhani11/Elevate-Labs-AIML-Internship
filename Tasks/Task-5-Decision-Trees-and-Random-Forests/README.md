# Task 5 - Decision Trees and Random Forests

## Objective

Learn and implement tree-based models for classification, including Decision Trees and Random Forests. The project also analyzes overfitting, controls tree depth, interprets feature importance, and evaluates model performance using cross-validation.

## Dataset

The project uses the Heart Disease dataset provided as `heart.csv`.

- Original rows: 1025
- Columns: 14
- Features: 13
- Target: `target`
- Missing values: 0
- Duplicate rows removed: 723
- Rows after removing duplicates: 302

Target classes:
- `0` = No Disease
- `1` = Disease

## Methodology

1. Loaded and inspected the Heart Disease dataset.
2. Checked missing values and duplicate rows.
3. Removed 723 exact duplicate rows.
4. Separated features and target.
5. Split the data into training and testing sets using an 80:20 stratified split with `random_state=42`.
6. Trained and visualized a Decision Tree Classifier.
7. Analyzed overfitting using different `max_depth` values.
8. Controlled the tree depth using `max_depth=3`.
9. Trained a Random Forest Classifier with 100 trees.
10. Compared Decision Tree and Random Forest accuracy.
11. Calculated and visualized Random Forest feature importances.
12. Evaluated the controlled Decision Tree using 5-fold cross-validation.

## Decision Tree Results

Initial Decision Tree Test Accuracy:

**80.33%**

### Depth Analysis

| Max Depth | Training Accuracy | Testing Accuracy |
|---:|---:|---:|
| 1 | 78.4% | 65.6% |
| 2 | 78.4% | 65.6% |
| 3 | 85.9% | 80.3% |
| 4 | 87.1% | 72.1% |
| 5 | 94.2% | 77.0% |
| 6 | 96.3% | 77.0% |
| 7 | 97.9% | 77.0% |
| 8 | 99.6% | 78.7% |
| 10 | 100.0% | 80.3% |
| None | 100.0% | 80.3% |

As tree depth increases, training accuracy rises substantially while testing accuracy does not improve consistently. Deeper trees reaching 100% training accuracy while remaining around 80% on the test set indicate a risk of overfitting.

The controlled Decision Tree with `max_depth=3` achieved **80.33%** test accuracy while keeping the model simpler.

## Random Forest Results

Random Forest configuration:

- `n_estimators=100`
- `random_state=42`

Test Accuracy:

**75.41%**

### Model Comparison

| Model | Test Accuracy |
|---|---:|
| Decision Tree (`max_depth=3`) | **80.33%** |
| Random Forest (`n_estimators=100`) | **75.41%** |

For this particular train/test split, the controlled Decision Tree achieved higher test accuracy than the Random Forest.

## Feature Importance

Random Forest feature importance:

| Feature | Importance |
|---|---:|
| `cp` | 0.1740 |
| `thalach` | 0.1316 |
| `ca` | 0.1057 |
| `oldpeak` | 0.0966 |
| `thal` | 0.0904 |
| `age` | 0.0830 |
| `exang` | 0.0737 |
| `trestbps` | 0.0721 |
| `chol` | 0.0674 |
| `sex` | 0.0402 |
| `slope` | 0.0298 |
| `restecg` | 0.0243 |
| `fbs` | 0.0112 |

`cp` had the highest feature importance, while `fbs` had the lowest. Feature importance represents relative usefulness within the trained model and does not by itself establish causation.

## Cross-Validation

A 5-fold cross-validation was performed using the controlled Decision Tree (`max_depth=3`).

Cross-validation scores:

```text
[0.8033, 0.8197, 0.9000, 0.6833, 0.7667]
```

- Mean Cross-Validation Accuracy: **79.46%**
- Standard Deviation: **7.07%**

The average cross-validation accuracy was approximately 79.46%, with some variation between folds.

## Tools and Libraries

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook

## Repository Contents

- `Task_5_Decision_Trees_and_Random_Forests.ipynb` - Complete implementation, visualizations, evaluation, and analysis
- `heart.csv` - Dataset used for the project
- `README.md` - Project documentation

## Conclusion

This project demonstrates Decision Tree and Random Forest classification using the Heart Disease dataset. The controlled Decision Tree achieved **80.33%** test accuracy, while the Random Forest achieved **75.41%** on the same test split. Depth analysis demonstrated the risk of overfitting in deeper trees. The `max_depth=3` Decision Tree achieved 80.33% test accuracy and a mean 5-fold cross-validation accuracy of 79.46%.
