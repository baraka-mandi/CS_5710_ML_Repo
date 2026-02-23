# Author: Baraka Mandi

# Class: Machine Learning (CS 5710)

# Machine Learning Homework 2: Programming Component

Hw2 notebook contains the implementation and analysis for **Part B (Questions 7-9)** of Homework 2, focusing on Decision Trees and k-Nearest Neighbors (kNN) using the Iris dataset.

## Table of Contents
- [Q7: Decision Tree Analysis](#q7-decision-tree-analysis)
- [Q8: kNN Decision Boundaries](#q8-knn-decision-boundaries)
- [Q9: Performance Evaluation](#q9-performance-evaluation)

---

## Q7: Decision Tree Analysis
**Objective:** Evaluate the impact of `max_depth` on the `DecisionTreeClassifier` to identify underfitting and overfitting.

### Results
| Max Depth | Training Accuracy | Test Accuracy | Status |
| :--- | :--- | :--- | :--- |
| 1 | 0.667 | 0.644 | **Underfitting**: Model is too simple to capture class differences. |
| 2 | 0.943 | 0.933 | **Optimal**: High accuracy on both sets with good generalization. |
| 3 | 0.971 | 1.000 | **Highly Specific**: Approaches perfect classification for this split. |

**Discussion:** Increasing depth allows the tree to create more specific rules. At `max_depth=1`, the model suffers from high bias (underfitting). As depth increases, the model complexity matches the data better, though excessive depth on noisier datasets can lead to high variance (overfitting).

---

## Q8: kNN Decision Boundaries
**Objective:** Visualize how the parameter `k` (number of neighbors) affects the decision boundary smoothness using Sepal length and width.



### Observations
- **k=1:** The boundary is highly irregular (jagged) and sensitive to individual data points. This represents a high-variance model.
- **k=10:** The boundary becomes significantly smoother and more linear, representing a model with higher bias but better stability against noise.

---

## Q9: Performance Evaluation
**Objective:** Use a Confusion Matrix and ROC Curves to provide a comprehensive evaluation of the kNN model ($k=5$).

### 1. Confusion Matrix
The confusion matrix tracks exactly where the model succeeds and where it confuses species (e.g., misclassifying Versicolor as Virginica).



### 2. ROC and AUC
Since Iris is a multi-class problem, we utilize a **One-vs-Rest (OvR)** approach to calculate the Receiver Operating Characteristic (ROC) and Area Under the Curve (AUC) for each species.



**Metric Interpretation:**
- **Accuracy:** Overall correctness of the model.
- **F1-Score:** Useful balance between Precision and Recall, especially if class distribution were uneven.
- **AUC Score:** A score near 1.0 (as seen in the Setosa class) indicates near-perfect separation capability.

---
