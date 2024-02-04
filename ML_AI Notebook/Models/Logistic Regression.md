**Prompt**: as a data scientist, teach me the Logistic Regression model in a detail-oriented way, with formulas, graphs, assumptions, optimization techniques, and implementation, how to use for binary classification and multi-class classification, when to use this model, when to avoid it, code examples, and recommend some research papers to read about it. cite your sources too.

Logistic Regression is a statistical method used for binary classification. It predicts the probability of a binary outcome (1/0, Yes/No, True/False) based on one or more predictor variables.

### Formula
The logistic regression function is defined as:
$\[ P(Y=1) = \frac{1}{1 + e^{-(\beta_0 + \beta_1 X)}} \]$
where \( P(Y=1) \) is the probability of the dependent variable equaling a "success" or "case" and \( e \) is the base of the natural logarithm.

### Assumptions
1. **Binary Outcome**: Dependent variable is binary.
2. **Independence**: Observations are independent.
3. **Linearity**: Linear relationship between the logit of the outcome and the predictors.
4. **No Multicollinearity**: Predictors shouldn't be highly correlated.

### Optimization Techniques
- **Maximum Likelihood Estimation (MLE)**: Used to estimate the parameters.

### Implementation
- **Binary Classification**: Used directly with binary outcomes.
- **Multi-class Classification**: Extended using methods like 'one-vs-rest'.

### Usage
- **When to Use**: Suitable for binary/multiclass classification tasks, especially with interpretable feature importance.
- **When to Avoid**: Not ideal for continuous data, large number of categorical variables, or non-linear relationships.

### Code Example
```python
from sklearn.linear_model import LogisticRegression
from sklearn.model_selection import train_test_split

# Example dataset
X, y = # your dataset

# Split the data
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

# Create logistic regression model
model = LogisticRegression()
model.fit(X_train, y_train)

# Predictions
predictions = model.predict(X_test)
```

### Research Papers
- "Logistic Regression in Rare Events Data" by Gary King and Langche Zeng.
- "The Elements of Statistical Learning" by Hastie, Tibshirani, and Friedman.

These sources provide a deeper understanding of logistic regression, its mathematical foundations, and practical applications.