Evaluating the performance of regression models involves several key metrics that capture the difference between the predicted values and the actual values from the data. Here are the most commonly used metrics:

### 1. Mean Absolute Error (MAE)
- **Definition**: The average of the absolute differences between the predicted values and the actual values. It gives an idea of how wrong the predictions were.
- **Formula**: 
  $\[ MAE = \frac{1}{n} \sum_{i=1}^{n} |y_i - \hat{y}_i| \]$
- **Math Example**:
  - Actual values: \([3, -0.5, 2, 7]\)
  - Predicted values: \([2.5, 0.0, 2, 8]\)
  - $MAE: \( (|3-2.5| + |-0.5-0.0| + |2-2| + |7-8|) / 4 = 0.5 \)$

### 2. Mean Squared Error (MSE)
- **Definition**: The average of the squared differences between the predicted values and the actual values. It penalizes larger errors.
- **Formula**: 
  $\[ MSE = \frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2 \]$
- **Math Example**:
  - Using the same values as above,
  - $MSE: \( ((3-2.5)^2 + (-0.5-0.0)^2 + (2-2)^2 + (7-8)^2) / 4 = 0.375 \)$

### 3. Root Mean Squared Error (RMSE)
- **Definition**: The square root of the MSE. It is in the same units as the response variable and gives a relatively high weight to large errors.
- **Formula**: 
  $\[ RMSE = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (y_i - \hat{y}_i)^2} \]$
- **Math Example**:
  - Using the same values as above,
  - $RMSE: \( \sqrt{0.375} \approx 0.612 \)$

### 4. R-squared (Coefficient of Determination)
- **Definition**: Represents the proportion of the variance for the dependent variable that's explained by the independent variables in the model. It provides an indication of the goodness of fit of a set of predictions.
- **Formula**: 
  $\[ R^2 = 1 - \frac{\sum_{i=1}^{n} (y_i - \hat{y}_i)^2}{\sum_{i=1}^{n} (y_i - \bar{y})^2} \]$
- **Math Example**:
  - Not as straightforward to calculate manually due to the comparison with the variance of actual values, but higher values (closer to 1) indicate better fit.

### Code Examples
Using Python's `scikit-learn` to calculate these metrics:

```python
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score
import numpy as np

# Actual and predicted values
y_true = np.array([3, -0.5, 2, 7])
y_pred = np.array([2.5, 0.0, 2, 8])

# Calculating metrics
mae = mean_absolute_error(y_true, y_pred)
mse = mean_squared_error(y_true, y_pred)
rmse = np.sqrt(mse)
r2 = r2_score(y_true, y_pred)

print(f"MAE: {mae}")
print(f"MSE: {mse}")
print(f"RMSE: {rmse}")
print(f"R-squared: {r2}")
```

### Conclusion
These metrics provide a comprehensive view of the model's performance, from general accuracy to the impact of outliers and the proportion of explained variance. It's essential to consider multiple metrics when evaluating a regression model to get a full picture of its predictive capabilities and limitations.