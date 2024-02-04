* [Start Here](https://www.analyticsvidhya.com/blog/2021/08/decision-tree-algorithm/)


### Decision Tree Machine Learning Algorithm

#### Concept
A Decision Tree is a flowchart-like tree structure where an internal node represents a feature(or attribute), the branch represents a decision rule, and each leaf node represents the outcome.

#### Mathematics & Formulas
1. **Splitting Criteria**:
   - **Gini Impurity**: A measure of purity/information gain. $\( Gini = 1 - \sum (p_i)^2 \)$ where \( p_i \) is the probability of an object being classified to a particular class.
   - **Entropy**: A measure of disorder or uncertainty. $\( Entropy = -\sum p_i \log_2(p_i) \)$.
   - **Information Gain**: The information that can increase the level of certainty after splitting. $\( IG = Entropy_{parent} - \sum \frac{N_{child}}{N} Entropy_{child} \).$

2. **Tree Pruning**: Reducing the size of the decision tree by removing parts of the tree that do not provide power to classify instances.

#### Visualization
Decision trees are visualized as flowcharts, which make them easy to interpret.

#### Pros and Cons
- **Pros**:
  - Easy to understand and interpret.
  - No need for feature scaling.
  - Can handle both numerical and categorical data.
  - Performs well with large datasets.

- **Cons**:
  - Prone to overfitting.
  - Unstable, as small variations in data can result in different trees.
  - Biased with imbalanced datasets.
  - Poor performance on tasks requiring complex relationships.

#### Assumptions
- Assumes that features are independent of each other.
- The structure of the tree changes with a change in the training data.

#### When to Use
- When the relationship between features and labels is approximately non-linear.
- When you need a quick baseline model.
- When interpretability is a significant requirement.

#### Suitable Data Type
- Categorical and Numerical.
- Works well with both small and large datasets.

#### Code Example in Python
```python
from sklearn.tree import DecisionTreeClassifier
from sklearn.model_selection import train_test_split
from sklearn.datasets import load_iris
from sklearn import tree
import matplotlib.pyplot as plt

# Load a dataset
iris = load_iris()
X, y = iris.data, iris.target

# Split the dataset
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2)

# Create and train a decision tree classifier
clf = DecisionTreeClassifier()
clf.fit(X_train, y_train)

# Predict the labels of the test set
y_pred = clf.predict(X_test)

# Visualize the decision tree
plt.figure(figsize=(12,12))
tree.plot_tree(clf, filled=True, feature_names=iris.feature_names, class_names=iris.target_names)
plt.show()
```

### Detailed Explanations of Key Concepts in Decision Trees

#### Entropy
1. **Concept**: 
   - Entropy, originating from information theory, measures the disorder or uncertainty in a dataset. 
   - In the context of a decision tree, it's used to quantify the impurity or randomness of an attribute.
2. **Formula**: 
   $\[ Entropy(S) = -\sum_{i=1}^{n} p_i \log_2(p_i) \]$
   - \( S \) is the dataset for which entropy is being calculated.
   - \( p_i \) is the proportion (probability) of the number of elements in class \( i \) to the number of elements in set \( S \).
3. **Example**: 
   - Suppose a dataset \( S \) has two classes (Yes and No), each class comprising 50% of the data. The entropy of \( S \) is calculated as:
   $\[ Entropy(S) = -(0.5 \log_2 0.5 + 0.5 \log_2 0.5) = 1 \]$
   - An entropy of 1 indicates maximum disorder.

#### Gini Index
1. **Concept**: 
   - Gini Index is a measure of impurity or purity used while creating a decision tree in the CART (Classification and Regression Tree) algorithm.
   - A Gini Index of 0 denotes that all elements belong to a single class, implying purity.
2. **Formula**: 
   $\[ Gini(S) = 1 - \sum_{i=1}^{n} p_i^2 \]$
   - \( p_i \) is the proportion of the elements that belong to class \( i \).
3. **Example**: 
   - For the same dataset \( S \) with two classes (50% each), the Gini Index is:
   $\[ Gini(S) = 1 - (0.5^2 + 0.5^2) = 0.5 \]$

#### Information Gain
1. **Concept**: 
   - Information Gain is the reduction in entropy or surprise by transforming a dataset and is often used in the ID3, C4.5, and C5.0 tree-generation algorithms.
   - It's the effectiveness of an attribute in classifying a dataset.
2. **Formula**: 
   $\[ IG(S, A) = Entropy(S) - \sum_{v \in Values(A)} \frac{|S_v|}{|S|} Entropy(S_v) \]$
   - \( A \) is the attribute for splitting.
   - \( S_v \) is the subset of \( S \) for which attribute \( A \) has value \( v \).
3. **Example**: 
   - If splitting by attribute \( A \) divides \( S \) into two subsets \( S_1 \) and \( S_2 \) with entropies 0.5 each, and each subset contains half of \( S \), then:
   $\[ IG(S, A) = 1 - \left(\frac{1}{2} \times 0.5 + \frac{1}{2} \times 0.5\right) = 0.5 \]$

#### Gain Ratio
1. **Concept**: 
   - Gain Ratio is a modification of the Information Gain that reduces its bias and is used in the C4.5 algorithm.
   - It normalizes Information Gain by using a Split Info value, which accounts for the number and size of branches.
2. **Formula**: 
   $\[ GainRatio(S, A) = \frac{IG(S, A)}{SplitInfo(S, A)} \]$
   $\[ SplitInfo(S, A) = -\sum_{v \in Values(A)} \frac{|S_v|}{|S|} \log_2\left(\frac{|S_v|}{|S|}\right) \]$
3. **Example**: 
   - Continuing the above example, if splitting by attribute \( A \) results in two equally sized subsets, then the Split Info would be:
   $\[ SplitInfo(S, A) = -2 \times \left(\frac{1}{2} \log_2 \frac{1}{2}\right) = 1 \]$
   - Hence, the Gain Ratio is \( 0.5 / 1 = 0.5 \).

### Python Code Example
```python
import numpy as np

# Entropy Function
def entropy(p):
    return -np.sum([pi * np.log2(pi) for pi in p if pi > 0])

# Gini Index Function
def gini(p):
    return 1 - sum([pi**2 for pi in p])

# Example Usage
p = [0.5, 0.5]  # Example probabilities
print

("Entropy:", entropy(p))
print("Gini Index:", gini(p))
```

### Conclusion
- **Entropy** and **Gini Index** are measures used to determine the best attribute for splitting the data in a decision tree.
- **Information Gain** evaluates the effectiveness of this attribute.
- **Gain Ratio** adjusts Information Gain to account for the size and number of branches, reducing bias towards attributes with more categories.
- Understanding these concepts is crucial for anyone working with decision tree algorithms in machine learning.