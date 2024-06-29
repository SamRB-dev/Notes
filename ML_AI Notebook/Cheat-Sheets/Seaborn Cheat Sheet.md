**New:**
```python
	seaborn.heatmap(features.corr(), annot=True, fmt= ".0%")
```
**Generate Multi plot grid**:
```python
fig, axs = plt.subplots(nrows=4, ncols=2, figsize=(16,9))
axs = axs.flatten()
for idx,column in enumerate(list):
	seaborn.boxplot(data=df[column], ax=axs[idx])
	axs[idx].set_title(column)
plt.tight_layout()
```
**Select columns of specific types**:
```python
numeric_col = df.select_dtypes(exclude="object").columns.tolist()
```

**Seaborn Basics:**
- Importing Seaborn:
  ```python
import seaborn as sns
  ```

**Data Visualization:**

- Line plot:
  ```python
  sns.lineplot(x='x_column', y='y_column', data=df)
  ```

- Bar plot:
  ```python
  sns.barplot(x='x_column', y='y_column', data=df)
  ```

- Histogram:
  ```python
  sns.histplot(data=df, x='column_name', kde=True)
  ```

- Scatter plot:
  ```python
  sns.scatterplot(x='x_column', y='y_column', data=df)
  ```

- Box plot:
  ```python
  sns.boxplot(x='x_column', y='y_column', data=df)
  ```

- Violin plot:
  ```python
  sns.violinplot(x='x_column', y='y_column', data=df)
  ```

- Heatmap:
  ```python
  sns.heatmap(data=df, cmap='coolwarm')
  ```

- Pair plot:
  ```python
  sns.pairplot(data=df)
  ```

**Styling and Customization:**

- Setting styles:
  ```python
  # Set the default theme
  sns.set_theme()

  # Set a specific theme
  sns.set_theme(style='whitegrid')
  ```

- Color palettes:
  ```python
  # Set the default color palette
  sns.set_palette('default')

  # Set a specific color palette
  sns.set_palette('pastel')
  ```

- Adding titles and labels:
  ```python
  # Set a title
  plt.title('Title')

  # Set x-axis label
  plt.xlabel('X Label')

  # Set y-axis label
  plt.ylabel('Y Label')
  ```

- Customizing plot appearance:
  ```python
  # Set plot size
  plt.figure(figsize=(10, 6))

  # Customize tick labels
  plt.xticks(rotation=45)
  plt.yticks(fontsize=12)

  # Add grid lines
  plt.grid(True)
  ```

**Additional Functionality:**

- Faceting and subplots:
  ```python
  # Facet grid
  g = sns.FacetGrid(data=df, col='column_name', row='row_column')
  g.map(sns.histplot, 'value_column')

  # Subplots
  fig, axes = plt.subplots(nrows, ncols)
  sns.histplot(data=df, ax=axes[row_index, col_index])
  ```

- Regression and trend lines:
  ```python
  # Scatter plot with regression line
  sns.regplot(x='x_column', y='y_column', data=df)

  # Scatter plot matrix with regression lines
  sns.pairplot(data=df, kind='reg')
  ```

- Annotations and text:
  ```python
  # Add text annotation
  plt.text(x, y, 'text')

  # Add value labels to bars
  for p in ax.patches:
      ax.annotate(format(p.get_height(), '.2f'), (p.get_x() + p.get_width() / 2., p.get_height()), ha = 'center', va = 'center', xytext = (0, 10), textcoords = 'offset points')
  ```

