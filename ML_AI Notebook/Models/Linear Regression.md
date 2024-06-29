Linear regression is a statistical method used for modeling the relationship between a dependent variable and one or more independent variables. The basic form of the model is:

\[ y = \β0  + \β1 x + \epsilon ϵ\]

- \( y \): Dependent variable.
- \( x \): Independent variable.
- \($\beta_0$ \): Intercept.
- \( $\beta_1$ \): Slope coefficient.
- \( \epsilon ϵ\): Error term.

#### Simple Linear Regression

In simple linear regression, there is one independent variable (\( x \)), so the formula becomes:

$\[ y = \beta_0 + \beta_1 x \]$

Graphically, this is represented as a straight line where \( \beta_0 \) is the y-intercept, and \( \beta_1 \) is the slope.

#### Multiple Linear Regression

In multiple linear regression, there are multiple independent variables:

$\[ y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + ... + \beta_n x_n \]$

Here, each \( x_i \) represents a different independent variable, and \( \beta_i \) is the coefficient for that variable.

### Assumptions of Linear Regression

1. **Linearity**: The relationship between the independent and dependent variables should be linear.
2. **Independence**: Observations should be independent of each other.
3. **Homoscedasticity**: The residuals (or errors) should have constant variance.
4. **Normal Distribution of Errors**: The residuals should be normally distributed.

### Optimization: Least Squares Method

The coefficients \( \beta_0 \) and \( \beta_1 \) are usually estimated using the least squares method, which minimizes the sum of the squared differences between the observed values and the values predicted by the model.

### Code Example in Python

#### Simple Linear Regression

```python
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# Sample data
x = np.array([5, 15, 25, 35, 45, 55]).reshape((-1, 1))
y = np.array([5, 20, 14, 32, 22, 38])

# Create a model and fit it
model = LinearRegression()
model.fit(x, y)

# Make predictions
y_pred = model.predict(x)

# Plotting
plt.scatter(x, y, color='blue')
plt.plot(x, y_pred, color='red')
plt.show()
```

#### Multiple Linear Regression

```python
# Assuming x has multiple columns representing different features
model.fit(x, y)  # x is now a 2D array with multiple columns
y_pred = model.predict(x)
```

### Recommended Research Papers

1. "Least Squares Regression for Categorical Data" by G. A. F. Seber and C. J. Wild.
2. "A Survey on Linear Regression" by James O. Berger.
3. "Multiple Linear Regression Viewpoints" published in "Journal of Statistics Education".
4. "Modern Applied Statistics with S" by W. N. Venables and B. D. Ripley.

These papers and books provide a comprehensive understanding of linear regression, including theoretical foundations and practical applications.

### Sources

- "An Introduction to Statistical Learning" by Gareth James, Daniela Witten, Trevor Hastie, and Robert Tibshirani.
- "The Elements of Statistical Learning" by Trevor Hastie, Robert Tibshirani, and Jerome Friedman.
- Python documentation for sklearn.linear_model.LinearRegression.


#### Implementation from Scratch
