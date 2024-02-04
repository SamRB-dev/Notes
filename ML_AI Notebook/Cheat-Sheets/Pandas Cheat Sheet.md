**Pandas Basics:**

- Importing Pandas:
  ```python
  import pandas as pd
  from ydata_profiling import ProfileReport
  ```

**Data Structures:**

- Series:
  ```python
  # Creating a Series
  series = pd.Series(data, index)
  ```

- DataFrame:
  ```python
  # Creating a DataFrame from a dictionary
  df = pd.DataFrame(data)

  # Creating a DataFrame from a NumPy array
  df = pd.DataFrame(data, columns)
  ```

**Data Exploration:**

- Basic information about the DataFrame:
  ```python
  # View the first few rows
  df.head()

  # View the last few rows
  df.tail()

  # Get summary statistics
  df.describe()
  df.describe(include="object")

  # Get the shape of the DataFrame
  df.shape

  # Get the column names
  df.columns

  # Get the index values
  df.index

  # Count the number of non-null values in each column
  df.info()
	
  # Check Unique Values
  df.unique()
	
  # List All Unique values and their total counts
  df.value_counts()

  # Change Dtype of a column
  df['col'] = df['col'].astype('type')
  ```

**Data Selection and Manipulation:**

- Selecting columns:
  ```python
  # Select a single column
  column = df['column_name']

  # Select multiple columns
  columns = df[['column_name1', 'column_name2']]
  ```

- Selecting rows:
  ```python
  # Select rows based on a condition
  filtered_df = df[df['column_name'] > threshold]

  # Select rows using loc (label-based indexing)
  selected_rows = df.loc[label]

  # Select rows using iloc (integer-based indexing)
  selected_rows = df.iloc[index]
  ```

- Creating new columns:
  ```python
  # Create a new column based on existing columns
  df['new_column'] = expression
  ```

- Aggregating data:
  ```python
  # Group by a column and calculate the mean
  grouped_data = df.groupby('column_name').mean()

  # Calculate the sum of a column
  sum_value = df['column_name'].sum()

  # Calculate the maximum value of a column
  max_value = df['column_name'].max()

  # Calculate the minimum value of a column
  min_value = df['column_name'].min()
  ```

**Data Cleaning:**

- Handling missing values:
  ```python
  # Check for missing values
  df.isnull()

  # Drop rows with missing values
  cleaned_df = df.dropna()

  # % of Missing Values
  df.isnull().sum().sum() / np.product(df.shape)*100

  # Fill missing values with a specified value
  filled_df = df.fillna(value)

  # Drop unnecessary columns
  df = df.drop(['Column1','Column2'],axis=1)

  # Drop rows with missing values
  df = df.dropna()
  
  # Replace missing values
  df["col"].replace(np.nan, new_val)
  
  # Replace other values
  df["col"].str.replace('old','new')

  ```

**Data Visualization:**

- Line plot:
  ```python
  df.plot(x='column_name', y='column_name', kind='line')
  ```

- Bar plot:
  ```python
  df.plot(x='column_name', y='column_name', kind='bar')
  ```

- Histogram:
  ```python
  df['column_name'].plot(kind='hist')
  df.hist(figsize=(15,10))
  ```

- Scatter plot:
  ```python
  df.plot(x='column_name', y='column_name', kind='scatter')
  ```

**Data Input and Output:**

- Reading and writing data:
  ```python
  # Read data from a CSV file
  df = pd.read_csv('file.csv')

  # Write data to a CSV file
  df.to_csv('file.csv', index=False)

  # Read data from an Excel file
  df = pd.read_excel('file.xlsx')

  # Write data to an Excel file
  df.to_excel('file.xlsx', index=False)
  ```

- Correlation Analysis with Heatmap
```python
	import seaborn as sns
	import matplotlib.pyplot as plt

	# Create correlation matrix[Pearson]
	corr_matrix = df.corr()

	# Set the figure size
	plt.figure(figsize=(10, 8))

	# Plot the correlation heatmap
	sns.heatmap(corr_matrix, annot=True)

	# Display the plot
	plt.show()
```


**Pandas Plotting Cheat Sheet**

**1. Line Plots:**
- `df.plot()` - Plot all columns as lines.
- `df.plot(x='column', y='column')` - Plot specific columns as lines.
- `df.plot.line()` - Line plot with various customization options.

**2. Bar Plots:**
- `df.plot.bar()` - Vertical bar plot.
- `df.plot.barh()` - Horizontal bar plot.
- `df.plot.bar(stacked=True)` - Stacked bar plot.

**3. Histograms:**
- `df.plot.hist()` - Plot histogram of each column.
- `df.plot.hist(alpha=0.5)` - Adjust transparency.
- `df.plot.hist(by='column')` - Histogram by column values.

**4. Scatter Plots:**
- `df.plot.scatter(x='column', y='column')` - Scatter plot.
- `df.plot.scatter(x='column', y='column', c='column', cmap='colormap')` - Color-coded scatter plot.

**5. Box Plots:**
- `df.plot.box()` - Box plot of each column.
- `df.plot.box(by='column')` - Box plot grouped by column values.
- `df.plot.box(vert=False)` - Horizontal box plot.

**6. Area Plots:**
- `df.plot.area()` - Stacked area plot.
- `df.plot.area(stacked=False)` - Unstacked area plot.

**7. Pie Charts:**
- `df.plot.pie()` - Pie chart of column values.
- `df.plot.pie(y='column')` - Pie chart of specific column values.
- `df.plot.pie(subplots=True)` - Pie chart for each column.

**8. Density Plots:**
- `df.plot.kde()` - Kernel Density Estimation plot.
- `df.plot.density()` - Density plot using Gaussian kernels.

**9. Boxen Plots:**
- `df.plot.boxen()` - Enhanced box plot with more quantiles.

**10. Hexbin Plots:**
- `df.plot.hexbin(x='column', y='column')` - Hexagonal bin plot.

**11. Customization:**
- `plt.title('Title')` - Set plot title.
- `plt.xlabel('X-axis label')` - Set x-axis label.
- `plt.ylabel('Y-axis label')` - Set y-axis label.
- `plt.xlim(start, end)` - Set x-axis limits.
- `plt.ylim(start, end)` - Set y-axis limits.
- `plt.legend()` - Show legend.
- `plt.grid(True)` - Show grid lines.
- `plt.savefig('filename.png')` - Save plot as an image file.

Remember to import the necessary libraries:
```python
import pandas as pd
import matplotlib.pyplot as plt
```


**Pandas Plotting Cheat Sheet**

**1. Scatter Matrix Plot:**
- `pd.plotting.scatter_matrix(df)` - Scatter matrix plot of all columns.
- `pd.plotting.scatter_matrix(df, diagonal='hist')` - Histogram on diagonal instead of scatter plot.

**2. Parallel Coordinates Plot:**
- `pd.plotting.parallel_coordinates(df, 'column')` - Parallel coordinates plot based on a specific column.

**3. Autocorrelation Plot:**
- `pd.plotting.autocorrelation_plot(series)` - Autocorrelation plot for a time series.

**4. Lag Plot:**
- `pd.plotting.lag_plot(series)` - Lag plot for a time series.

**5. Bootstrap Plot:**
- `pd.plotting.bootstrap_plot(series)` - Bootstrap plot for a time series.

**6. Andrews Curves:**
- `pd.plotting.andrews_curves(df, 'column')` - Andrews curves plot based on a specific column.

**7. RadViz Plot:**
- `pd.plotting.radviz(df, 'column')` - Radial visualization plot based on a specific column.

**8. Hexbin Plot:**
- `pd.plotting.hexbin(df, x='column', y='column')` - Hexagonal bin plot.

**9. Bootstrap Plots:**
- `pd.plotting.bootstrap_plot(series)` - Bootstrap plot for a time series.

**10. Lag Plot:**
- `pd.plotting.lag_plot(series)` - Lag plot for a time series.

**11. Andrews Curves:**
- `pd.plotting.andrews_curves(df, 'column')` - Andrews curves plot based on a specific column.

**12. RadViz Plot:**
- `pd.plotting.radviz(df, 'column')` - Radial visualization plot based on a specific column.

Remember to import the necessary libraries:
```python
import pandas as pd
import matplotlib.pyplot as plt
```
* * *
## Remember
- Pandas scatter_matrix can plot df aganist each attributes.
* * *
## **Data Cleaning Cheat Sheet**

1. **Handling Missing Values:**
   - Identify missing values: `df.isnull()` or `df.isna()`
   - Count missing values: `df.isnull().sum()` or `df.isna().sum()`
   - Remove rows with missing values: `df.dropna()`
   - Remove columns with missing values: `df.dropna(axis=1)`
   - Fill missing values with a specific value: `df.fillna(value)`
   - Fill missing values with mean, median, or mode: `df.fillna(df.mean())`, `df.fillna(df.median())`, `df.fillna(df.mode().iloc[0])`
   - Interpolate missing values: `df.interpolate()`

2. **Handling Duplicates:**
   - Identify duplicate rows: `df.duplicated()`
   - Remove duplicate rows: `df.drop_duplicates()`
   - Remove duplicates based on specific columns: `df.drop_duplicates(subset=['column1', 'column2'])`

3. **Data Transformation:**
   - Rename columns: `df.rename(columns={'old_name': 'new_name'})`
   - Change data types of columns: `df.astype({'column1': 'int', 'column2': 'float'})`
   - Apply a function to a column or DataFrame: `df['column'].apply(function)` or `df.apply(function)`

4. **Handling Outliers:**
   - Identify outliers using summary statistics: `df.describe()`
   - Visualize outliers using boxplots or histograms: `df.boxplot(column='column')`, `df.hist(column='column')`
   - Remove outliers based on z-scores: `df[(np.abs(stats.zscore(df['column'])) < threshold)]`
   - Winsorize outliers (replace outliers with certain percentiles): `scipy.stats.mstats.winsorize(df['column'], limits=(lower_limit, upper_limit))`

5. **Handling Inconsistent Data:**
   - Standardize text case: `df['column'].str.lower()` or `df['column'].str.upper()`
   - Remove leading/trailing whitespaces: `df['column'].str.strip()`
   - Replace incorrect values: `df.replace({'old_value': 'new_value'})`
   - Remove unwanted characters or patterns: `df['column'].str.replace('pattern', '')`
   - Extract relevant information using regular expressions: `df['column'].str.extract('pattern')`

6. **Data Imputation:**
   - Impute missing values with mean, median, or mode: `SimpleImputer(strategy='mean')`, `SimpleImputer(strategy='median')`, `SimpleImputer(strategy='most_frequent')`
   - Impute missing values with regression models: `IterativeImputer()`

7. **Handling Categorical Variables:**
   - Convert categorical variables to numerical using one-hot encoding: `pd.get_dummies(df['column'])`
   - Convert categorical variables to numerical using label encoding: `LabelEncoder()`

8. **Feature Scaling:**
   - Standardize features using z-score normalization: `StandardScaler()`
   - Scale features to a specified range: `MinMaxScaler(feature_range=(min_value, max_value))`
   - Normalize features using L1 or L2 normalization: `Normalizer(norm='l1')`, `Normalizer(norm='l2')`

9. **Date and Time Handling:**
   - Convert strings to date/time objects: `pd.to_datetime(df['column'], format='format_string')`
   - Extract components from date/time: `df['column'].dt.year`, `df['column'].dt.month`, `df['column'].dt.day`, etc.
   - Calculate time differences: `df['column1'] - df['column2']`

10. **Data Sampling:**
    - Randomly sample rows from a DataFrame: `df.sample(n=sample_size)` or `df.sample(frac=sample_fraction)`
    - Stratified sampling based on a categorical variable: `df.groupby('category').apply(lambda x: x.sample(n=sample_size))`

11. **Handling Skewed Data:**
    - Logarithmic transformation: `np.log()`
    - Box-Cox transformation: `scipy.stats.boxcox()`

12. **Data Integration:**
    - Concatenate DataFrames vertically: `pd.concat([df1, df2])`
    - Concatenate DataFrames horizontally: `pd.concat([df1, df2], axis=1)`
    - Merge DataFrames based on common columns: `pd.merge(df1, df2, on='column')`

Remember, data cleaning techniques may vary based on the specific dataset and problem at hand. It's important to analyze the data, understand its characteristics, and choose the appropriate cleaning methods accordingly.
* * *
