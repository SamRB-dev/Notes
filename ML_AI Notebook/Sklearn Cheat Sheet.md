**SKLEARN CHEAT SHEET**

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