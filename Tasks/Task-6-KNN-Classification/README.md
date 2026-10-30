# Task 6 - KNN Classification

## Objective

Implement K-Nearest Neighbors (KNN) for classification and understand instance-based learning, Euclidean distance, and the selection of an appropriate K value.

## Dataset

The Iris dataset was used for this task.

- Dataset: Iris Dataset
- Samples: 150
- Features used: Sepal Length, Sepal Width, Petal Length, Petal Width
- Target: Iris species
- Classes:
  - Iris-setosa
  - Iris-versicolor
  - Iris-virginica

The `Id` column was excluded because it is only an identifier and does not represent a flower feature.

## Methodology

1. Loaded and inspected the Iris dataset using Pandas.
2. Checked the dataset for missing values and duplicate rows.
3. Separated the input features and target variable.
4. Standardized the numerical features using `StandardScaler`.
5. Split the data into training and testing sets using an 80:20 ratio.
6. Implemented KNN using `KNeighborsClassifier`.
7. Tested multiple K values: 1, 3, 5, 7, 9, 11, 13, and 15.
8. Compared the accuracy obtained for each K value.
9. Selected K=7 for the final KNN model.
10. Evaluated the final model using accuracy and a confusion matrix.
11. Visualized KNN decision boundaries using Petal Length and Petal Width.

## Results

The tested K values produced the following test accuracies:

| K | Accuracy |
|---:|---:|
| 1 | 96.67% |
| 3 | 93.33% |
| 5 | 93.33% |
| 7 | 96.67% |
| 9 | 96.67% |
| 11 | 96.67% |
| 13 | 96.67% |
| 15 | 93.33% |

K=7 was selected as the final value because it achieved the highest observed test accuracy while providing a moderate neighborhood size.

### Final Model Performance

- Algorithm: K-Nearest Neighbors (KNN)
- K: 7
- Test Accuracy: 96.67%
- Correctly classified test samples: 29 out of 30

### Confusion Matrix

The final model classified:

- Iris-setosa: 10/10 correct
- Iris-versicolor: 10/10 correct
- Iris-virginica: 9/10 correct
- One Iris-virginica sample was classified as Iris-versicolor.

## Decision Boundary Visualization

A 2D decision boundary was created using standardized Petal Length and Petal Width. The visualization shows the regions predicted by the KNN model for the three Iris species.

The decision boundary is used for visualization only. The main final KNN model uses all four standardized flower measurement features.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

## Repository Contents

- `Task_6_KNN_Classification.ipynb` - Jupyter Notebook containing the complete implementation and visualizations.
- `Iris.csv` - Dataset used for classification.
- `README.md` - Project documentation.

## Conclusion

K-Nearest Neighbors (KNN) classification was successfully implemented on the Iris dataset.

The features were standardized before training so that all measurements were on a comparable scale. Different values of K were tested, and K=7 was selected for the final model.

The final KNN model achieved an accuracy of 96.67% on the test dataset. The confusion matrix showed that 29 out of 30 test samples were classified correctly.

The decision boundary visualization using Petal Length and Petal Width showed how KNN separates the three Iris species based on their feature values.

Overall, KNN performed well on the Iris classification problem.
