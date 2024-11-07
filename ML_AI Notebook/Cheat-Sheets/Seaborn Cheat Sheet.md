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


---

## Seaborn Cheat Sheet

### Installation and Import
```bash
pip install seaborn
```

```python
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd
import numpy as np
```

### Basic Plotting Functions

#### 1. **Scatter Plot**

```python
sns.scatterplot(data=df, x='x_column', y='y_column', hue='hue_column', style='style_column', size='size_column', palette='palette_name')
plt.show()
```

**Parameters:**
- `data`: DataFrame containing the data.
- `x`, `y`: Column names for the x and y axes.
- `hue`: Column name for color encoding.
- `style`: Column name for style encoding (e.g., markers).
- `size`: Column name for size encoding.
- `palette`: Color palette.

#### 2. **Line Plot**

```python
sns.lineplot(data=df, x='x_column', y='y_column', hue='hue_column', style='style_column', size='size_column', palette='palette_name')
plt.show()
```

**Parameters:**
- Similar to `scatterplot`.

#### 3. **Bar Plot**

```python
sns.barplot(data=df, x='x_column', y='y_column', hue='hue_column', palette='palette_name')
plt.show()
```

**Parameters:**
- Similar to `scatterplot`.

#### 4. **Histogram**

```python
sns.histplot(data=df, x='x_column', hue='hue_column', multiple='stack', kde=True, bins=30, palette='palette_name')
plt.show()
```

**Parameters:**
- `multiple`: `'layer'`, `'dodge'`, `'stack'`, `'fill'`.
- `kde`: Whether to plot a kernel density estimate.
- `bins`: Number of bins.

#### 5. **Box Plot**

```python
sns.boxplot(data=df, x='x_column', y='y_column', hue='hue_column', palette='palette_name')
plt.show()
```

**Parameters:**
- Similar to `scatterplot`.

#### 6. **Violin Plot**

```python
sns.violinplot(data=df, x='x_column', y='y_column', hue='hue_column', split=True, palette='palette_name')
plt.show()
```

**Parameters:**
- `split`: Whether to split the violins for different levels of the hue variable.

#### 7. **Pair Plot**

```python
sns.pairplot(df, hue='hue_column', palette='palette_name', markers=['o', 's', 'D'])
plt.show()
```

**Parameters:**
- `markers`: List of marker styles.

#### 8. **Heatmap**

```python
sns.heatmap(data=df.corr(), annot=True, cmap='coolwarm')
plt.show()
```

**Parameters:**
- `data`: 2D dataset.
- `annot`: Annotate each cell with the numeric value.
- `cmap`: Colormap.

#### 9. **FacetGrid**

```python
g = sns.FacetGrid(df, col='column', hue='hue_column', palette='palette_name', height=4, aspect=0.8)
g.map(plt.hist, 'x_column', bins=20, alpha=0.7)
g.add_legend()
plt.show()
```

**Parameters:**
- `col`, `row`: Variables that define subsets of the data, column-wise or row-wise.
- `hue`: Variable for color encoding.
- `height`: Height of each facet.
- `aspect`: Aspect ratio of each facet.

### Customization and Styling

#### 1. **Setting Style**

```python
sns.set_style('whitegrid')  # Options: 'white', 'dark', 'whitegrid', 'darkgrid', 'ticks'
```

#### 2. **Color Palettes**

```python
sns.set_palette('pastel')  # Options: 'deep', 'muted', 'bright', 'pastel', 'dark', 'colorblind'
```

#### 3. **Context**

```python
sns.set_context('notebook')  # Options: 'paper', 'notebook', 'talk', 'poster'
```

#### 4. **Customizing Axes**

```python
plt.xlabel('X-axis Label')
plt.ylabel('Y-axis Label')
plt.title('Plot Title')
plt.xticks(rotation=45)
plt.yticks(rotation=45)
```

#### 5. **Legend**

```python
plt.legend(title='Legend Title', loc='best')  # loc: 'best', 'upper right', 'upper left', 'lower left', 'lower right'
```

### Example Workflow

```python
import seaborn as sns
import matplotlib.pyplot as plt
import pandas as pd

# Load dataset
df = sns.load_dataset('iris')

# Set style and context
sns.set_style('whitegrid')
sns.set_context('notebook')

# Create a scatter plot
sns.scatterplot(data=df, x='sepal_length', y='sepal_width', hue='species', style='species', palette='muted')
plt.xlabel('Sepal Length')
plt.ylabel('Sepal Width')
plt.title('Iris Sepal Dimensions')
plt.legend(title='Species', loc='upper right')
plt.show()
```

### Saving the Plot

```python
plt.savefig('plot.png', dpi=300, bbox_inches='tight')
```

**Parameters:**
- `dpi`: Resolution in dots per inch.
- `bbox_inches`: Bounding box in inches (`'tight'` is useful for removing extra white space).

### Seaborn Functions Overview

#### Distribution Plots

- **`sns.histplot()`**: Plot a histogram.
- **`sns.kdeplot()`**: Plot a kernel density estimate.
- **`sns.rugplot()`**: Plot datapoints in an array as sticks on an axis.
- **`sns.ecdfplot()`**: Plot empirical cumulative distribution functions.

#### Categorical Plots

- **`sns.boxplot()`**: Create a box plot.
- **`sns.violinplot()`**: Create a violin plot.
- **`sns.stripplot()`**: Create a scatter plot for categorical data.
- **`sns.swarmplot()`**: Create a scatter plot with non-overlapping points.
- **`sns.barplot()`**: Create a bar plot.
- **`sns.countplot()`**: Create a count plot.
- **`sns.pointplot()`**: Create a point plot.

#### Relational Plots

- **`sns.relplot()`**: Create a relational plot.
- **`sns.scatterplot()`**: Create a scatter plot.
- **`sns.lineplot()`**: Create a line plot.

#### Matrix Plots

- **`sns.heatmap()`**: Create a heatmap.
- **`sns.clustermap()`**: Create a clustered heatmap.

#### Pairwise Plots

- **`sns.pairplot()`**: Create pairwise plots.
- **`sns.jointplot()`**: Create a joint plot.

---


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

