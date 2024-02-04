
### Scikit-learn Cheat Sheet

#### 1. **Data Preprocessing**

   - **StandardScaler**: Standardize features by removing the mean and scaling to unit variance.
     - **Use case**: Before applying machine learning algorithms like SVM, k-nearest neighbors.
   - **MinMaxScaler**: Scale features to a given range, often between zero and one.
     - **Use case**: When you need non-distorted normalized features.
   - **LabelEncoder**: Encode target labels with value between 0 and n_classes-1.
     - **Use case**: Encoding categorical target variables.
   - **OneHotEncoder**: Encode categorical features as a one-hot numeric array.
     - **Use case**: When handling categorical data for algorithms that require numerical input.
   - **train_test_split**: Split arrays or matrices into random train and test subsets.
     - **Use case**: To evaluate the performance of your machine learning model.

#### 2. **Supervised Learning**

   - **LinearRegression**: Ordinary least squares Linear Regression.
     - **Use case**: Predicting a continuous-valued attribute (regression).
   - **LogisticRegression**: Logistic Regression (aka logit, MaxEnt) classifier.
     - **Use case**: Binary classification problems.
   - **DecisionTreeClassifier**: A decision tree classifier.
     - **Use case**: Classification tasks with complex datasets, where relationships may not be linear.
   - **RandomForestClassifier**: A random forest classifier.
     - **Use case**: Solving both classification and regression tasks.
   - **SVM (Support Vector Machines)**: C-Support Vector Classification.
     - **Use case**: Classification and regression (SVC, NuSVC, SVR).

#### 3. **Unsupervised Learning**

   - **KMeans**: K-Means clustering.
     - **Use case**: Data clustering.
   - **PCA (Principal Component Analysis)**: Linear dimensionality reduction.
     - **Use case**: Reducing the dimensionality of data, visualization.

#### 4. **Model Evaluation**

   - **cross_val_score**: Evaluate a score by cross-validation.
     - **Use case**: To get an estimate of a model’s performance.
   - **GridSearchCV**: Exhaustive search over specified parameter values for an estimator.
     - **Use case**: To find the best parameters for model tuning.
   - **confusion_matrix**: Compute confusion matrix to evaluate the accuracy of a classification.
     - **Use case**: Performance measurement for machine learning classification.
   - **roc_auc_score**: Compute Area Under the Receiver Operating Characteristic Curve (ROC AUC) from prediction scores.
     - **Use case**: Evaluation of classification models at various threshold settings.

#### 5. **Pipelines**

   - **Pipeline**: Pipeline of transforms with a final estimator.
     - **Use case**: Sequentially applying a list of transforms and a final estimator.

#### 6. **Utility Functions**

   - **fetch_openml**: Load a dataset from OpenML.
     - **Use case**: To import datasets for experimentation.
   - **make_classification/make_regression**: Generate a random n-class classification problem / Generate a random regression problem.
     - **Use case**: To create test datasets.

### Example Usage:

```python
from sklearn.ensemble import RandomForestClassifier
from sklearn.model_selection import train_test_split
from sklearn.metrics import accuracy_score
from sklearn.datasets import load_iris

# Load dataset
iris = load_iris()
X, y = iris.data, iris.target

# Split dataset
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42)

# Initialize classifier
clf = RandomForestClassifier(n_estimators=100)

# Train model
clf.fit(X_train, y_train)

# Predict
y_pred = clf.predict(X_test)

# Evaluate model
print(f"Accuracy: {accuracy_score(y_test, y_pred)}")
```

### Conclusion

This cheat sheet covers the basics of sklearn's functionalities, from data preprocessing to complex model evaluation. Remember, sklearn is a versatile library, and its full potential is realized through experimentation and practice in diverse scenarios.


---

1. **Data Preparation**:
   - Loading Data: `sklearn.datasets.load_*`
   - Splitting Data: `sklearn.model_selection.train_test_split`
   - Scaling Data: `sklearn.preprocessing.StandardScaler`
   - Encoding Categorical Data: `sklearn.preprocessing.OneHotEncoder`

2. **Supervised Learning**:
   - Regression Models:
     - Linear Regression: `sklearn.linear_model.LinearRegression`
     - Decision Tree Regression: `sklearn.tree.DecisionTreeRegressor`
     - Random Forest Regression: `sklearn.ensemble.RandomForestRegressor`
   - Classification Models:
     - Logistic Regression: `sklearn.linear_model.LogisticRegression`
     - Decision Tree Classifier: `sklearn.tree.DecisionTreeClassifier`
     - Random Forest Classifier: `sklearn.ensemble.RandomForestClassifier`

3. **Model Evaluation**:
   - Cross-Validation: `sklearn.model_selection.cross_val_score`
   - Grid Search: `sklearn.model_selection.GridSearchCV`
   - Model Evaluation Metrics:
     - Regression: `sklearn.metrics.mean_squared_error`, `sklearn.metrics.r2_score`
     - Classification: `sklearn.metrics.accuracy_score`, `sklearn.metrics.precision_score`, `sklearn.metrics.recall_score`, `sklearn.metrics.f1_score`

4. **Unsupervised Learning**:
   - Clustering:
     - K-Means: `sklearn.cluster.KMeans`
     - Hierarchical Clustering: `sklearn.cluster.AgglomerativeClustering`
   - Dimensionality Reduction:
     - Principal Component Analysis (PCA): `sklearn.decomposition.PCA`
     - t-Distributed Stochastic Neighbor Embedding (t-SNE): `sklearn.manifold.TSNE`

5. **Pipeline and Feature Selection**:
   - Pipelines: `sklearn.pipeline.Pipeline`
   - Feature Selection:
     - SelectKBest: `sklearn.feature_selection.SelectKBest`
     - Recursive Feature Elimination: `sklearn.feature_selection.RFE`

6. **Ensemble Methods**:
   - Bagging:
     - BaggingRegressor: `sklearn.ensemble.BaggingRegressor`
     - BaggingClassifier: `sklearn.ensemble.BaggingClassifier`
   - Boosting:
     - Gradient Boosting Regressor: `sklearn.ensemble.GradientBoostingRegressor`
     - Gradient Boosting Classifier: `sklearn.ensemble.GradientBoostingClassifier`
   - Voting: `sklearn.ensemble.VotingClassifier`, `sklearn.ensemble.VotingRegressor`
   - Stacking: `sklearn.ensemble.StackingClassifier`, `sklearn.ensemble.StackingRegressor`

7. **Model Persistence**:
   - Saving Models: `joblib.dump`
   - Loading Models: `joblib.load`

8. **Preprocessing and Pipelining**:
   - Feature Scaling: `sklearn.preprocessing.StandardScaler`, `sklearn.preprocessing.MinMaxScaler`
   - Feature Transformation: `sklearn.preprocessing.PolynomialFeatures`
   - Feature Union: `sklearn.pipeline.FeatureUnion`

9. **Text Processing**:
   - Text Vectorization: `sklearn.feature_extraction.text.CountVectorizer`, `sklearn.feature_extraction.text.TfidfVectorizer`
   - Text Classification: `sklearn.feature_extraction.text.HashingVectorizer`

10. **Model Selection**:
    - Cross-Validation: `sklearn.model_selection.KFold`, `sklearn.model_selection.StratifiedKFold`
    - Hyperparameter Tuning: `sklearn.model_selection.GridSearchCV`, `sklearn.model_selection.RandomizedSearchCV`

Remember, this cheat sheet provides an overview of common functionalities and methods in scikit-learn, but it's always important to consult the official documentation for more detailed information and usage examples.