**NumPy Basics:**

- Importing NumPy:
  ```python
  import numpy as np
  ```

- Creating NumPy arrays:
  ```python
  # From a Python list
  arr = np.array([1, 2, 3, 4, 5])

  # With a range of values
  arr = np.arange(start, stop, step)

  # With a specified shape filled with zeros
  zeros_arr = np.zeros(shape)

  # With a specified shape filled with ones
  ones_arr = np.ones(shape)

  # With a specified shape filled with a constant value
  constant_arr = np.full(shape, value)

  # With random values from a uniform distribution between 0 and 1
  random_arr = np.random.rand(shape)
  ```

- Accessing array elements:
  ```python
  # Single element
  arr[index]

  # Slicing
  arr[start:stop:step]
  ```

- Array shape and dimensions:
  ```python
  # Get the shape of an array
  arr.shape

  # Get the number of dimensions
  arr.ndim

  # Reshape an array
  reshaped_arr = arr.reshape(new_shape)
  ```

- Array operations:
  ```python
  # Element-wise operations
  result = arr1 + arr2
  result = arr1 - arr2
  result = arr1 * arr2
  result = arr1 / arr2

  # Dot product
  result = np.dot(arr1, arr2)

  # Transpose
  transposed_arr = arr.T

  # Concatenate arrays
  concatenated_arr = np.concatenate([arr1, arr2], axis)
  ```

**Array Manipulation:**

- Indexing and slicing:
  ```python
  # Access single element
  arr[row_index, column_index]

  # Slice a portion of an array
  sliced_arr = arr[start:stop:step, start:stop:step]

  # Access entire rows or columns
  row = arr[row_index, :]
  column = arr[:, column_index]
  ```

- Reshaping arrays:
  ```python
  # Reshape an array
  reshaped_arr = arr.reshape(new_shape)

  # Flatten an array
  flattened_arr = arr.flatten()

  # Transpose an array
  transposed_arr = arr.T
  ```

- Stacking arrays:
  ```python
  # Vertical stacking
  stacked_arr = np.vstack([arr1, arr2])

  # Horizontal stacking
  stacked_arr = np.hstack([arr1, arr2])
  ```

**Array Computations:**

- Statistical functions:
  ```python
  # Mean
  mean_value = np.mean(arr)

  # Median
  median_value = np.median(arr)

  # Standard deviation
  std_dev = np.std(arr)

  # Minimum and maximum
  min_value = np.min(arr)
  max_value = np.max(arr)

  # Sum
  sum_value = np.sum(arr)
  ```

- Mathematical functions:
  ```python
  # Square root
  sqrt_arr = np.sqrt(arr)

  # Exponential
  exp_arr = np.exp(arr)

  # Logarithm
  log_arr = np.log(arr)

  # Trigonometric functions
  sin_arr = np.sin(arr)
  cos_arr = np.cos(arr)
  ```

**Array Filtering:**

- Boolean indexing:
  ```python
  # Get elements satisfying a condition
  filtered_arr = arr[arr > threshold]

  # Use logical operators for complex conditions
  filtered_arr = arr[(arr > threshold1) & (arr < threshold2)]
  ```

- Nonzero elements:
  ```python
  # Get indices of nonzero elements
  indices = np.nonzero(arr)

  # Get nonzero elements
  nonzero_values = arr[indices]
  ```

