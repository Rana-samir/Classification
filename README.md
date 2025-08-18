# Bank Customer Churn Prediction

This project applies four classification models to predict whether a customer will exit the bank. The goal is to evaluate and compare the models in order to identify the most suitable one for this dataset.

## Findings

### K-Nearest Neighbors (KNN)

- KNN proved to be very suitable for this dataset, especially because it performs well on smaller datasets with distinct patterns.

- Challenges such as imbalanced data, noise in the Age column, and unscaled features were resolved to improve its performance.

- It is simple and does not require extensive parameter tuning, avoiding the high complexity of techniques like grid search.

- KNN works effectively even when data relationships are non-linear. Since linear correlation in the dataset was weak, KNN captured these non-linear relationships better.

- Additionally, KNN provides useful insights by identifying customers with similar behavioral patterns.

### Naive Bayes

- Naive Bayes assumes conditional independence between features, which does not hold true for this dataset.
For example, the number of products a customer holds often depends on whether they are active, creating dependencies among features.

- Because of these dependencies, Naive Bayes performed poorly, resulting in lower accuracy compared to other models.

### Decision Tree

- Decision Trees handled the churn dataset fairly well, providing reasonable accuracy across different features.

- Their performance, however, depends heavily on data quality and feature engineering.

- Since decision trees evaluate many parameters during splitting, they introduce slightly higher computational complexity.

### Support Vector Machine (SVM)

- SVM was effective but computationally expensive, especially when combined with grid search for hyperparameter tuning.

- It has the flexibility to classify both linear and non-linear data. In this case, the RBF kernel produced the best results, confirming the presence of non-linear relationships in the dataset.

### Conclusion
The best model for this dataset is KNN. While it ranked third in raw accuracy compared to other models, its simplicity, interpretability, and ability to handle non-linear relationships make it a strong choice. Its accuracy and F1 score are acceptable and provide a good balance between performance and complexity.
