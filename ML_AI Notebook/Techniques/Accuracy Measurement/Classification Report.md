#### Definition
A Classification Report is a performance evaluation metric in machine learning that is used to measure the quality of predictions from a classification algorithm. It shows the main classification metrics: precision, recall, and F1-score on a per-class basis.

#### Key Metrics
1. **Precision**: Indicates the proportion of positive identifications that were actually correct. It is defined as:
   $\[ \text{Precision} = \frac{TP}{TP + FP} \]$
   
2. **Recall (Sensitivity)**: Indicates how many actual positive cases were correctly identified. It is defined as:
   $\[ \text{Recall} = \frac{TP}{TP + FN} \]$

3. **F1-Score**: A weighted average of precision and recall. It is especially useful when the class distribution is imbalanced. Defined as:
   $\[ \text{F1 Score} = 2 \times \frac{\text{Precision} \times \text{Recall}}{\text{Precision} + \text{Recall}} \]$

4. **Support**: The number of actual occurrences of the class in the dataset.

#### Examples
Consider a binary classification for a disease detection system:
- **Precision**: Of all patients we diagnosed as having the disease, what proportion actually had the disease?
- **Recall**: Of all patients that actually had the disease, what proportion did we correctly diagnose?
- **F1-Score**: Balance between precision and recall.

#### Pros and Cons
- **Pros**:
  - Provides a more comprehensive view than accuracy alone, especially with imbalanced datasets.
  - Helps in understanding the trade-off between recall and precision for different classes.

- **Cons**:
  - Does not provide insights into the true negatives.
  - In multi-class problems, the report can become large and complex.

#### Python Code Example
```python
from sklearn.metrics import classification_report
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import train_test_split
from sklearn.datasets import load_iris

# Load a dataset
X, y = load_iris(return_X_y=True)

# Split the dataset
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3)

# Train a logistic regression model
model = LogisticRegression(max_iter=200)
model.fit(X_train, y_train)

# Make predictions
y_pred = model.predict(X_test)

# Generate and print classification report
print(classification_report(y_test, y_pred))
```

In this code, `classification_report` from `sklearn.metrics` is used to generate a detailed classification report for a logistic regression model trained on the Iris dataset.

#### Conclusion
A classification report is an essential tool for understanding the performance of classification models, particularly in scenarios where balancing different types of errors is crucial. It provides a more nuanced view than accuracy alone, making it especially useful for models trained on imbalanced datasets.