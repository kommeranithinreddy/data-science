# NumPy

Practical work with **NumPy** for numerical computing, array operations, statistical calculations, and data processing in Python.

This notebook covers essential NumPy operations and demonstrates their application to numerical data analysis.

## Topics Covered

### 1. Arrays and Fundamentals

- Creating arrays with `np.array()`
- Array creation using:
  - `np.zeros()`
  - `np.ones()`
  - `np.full()`
  - `np.arange()`
  - `np.linspace()`
- Array properties: `shape`, `ndim`, `size`, and `dtype`
- One-dimensional and two-dimensional arrays
- Indexing and slicing
- Updating array values

### 2. Operations, Aggregation, and Filtering

- Element-wise arithmetic and array-to-array operations
- Comparison operations
- Aggregation functions:
  - `sum()`
  - `mean()`
  - `median()`
  - `min()`
  - `max()`
  - `std()`
  - `var()`
- Understanding the `axis` parameter
- Boolean filtering
- Combining conditions using `&` and `|`
- Conditional selection with `np.where()`
- Handling `NaN` values

### 3. Reshaping and Combining Arrays

- Reshaping arrays with `reshape()`
- Using `-1` for automatic dimension inference
- Converting arrays to one dimension with `flatten()` and `ravel()`
- Transposing arrays with `.T`
- Combining arrays with `np.concatenate()`
- Stacking arrays with `np.stack()`
- Understanding concatenation versus stacking

### 4. Broadcasting and Vectorization

- Understanding vectorization
- Scalar broadcasting
- Broadcasting between arrays
- Broadcasting rules and shape compatibility
- Right-to-left dimension matching
- Performing operations without explicit Python loops

### 5. Random Numbers and Statistics

- Creating random number generators with `np.random.default_rng()`
- Generating random integers with `rng.integers()`
- Generating random floating-point numbers with `rng.random()`
- Random sampling with `rng.choice()`
- Generating normally distributed values with `rng.normal()`
- Random seeds and reproducibility
- Statistical calculations
- Percentiles

### 6. Basic Linear Algebra

- Dot products
- Matrix multiplication
- `np.dot()`
- The `@` operator
- `np.matmul()`
- Element-wise multiplication versus matrix multiplication
- Matrix shape compatibility
- Representing numerical features as matrices

### 7. Integrated Data Science Exercise

A practical exercise combining multiple NumPy concepts:

- Handling missing values
- Aggregation and filtering
- Broadcasting
- Percentile calculations
- Weighted calculations
- Matrix multiplication
- Numerical data analysis

## Key Concepts

### Axis

For a two-dimensional array:

```text
shape = (rows, columns)

axis=0 → operations across rows, producing column-wise results
axis=1 → operations across columns, producing row-wise results
```

For concatenation:

```text
axis=0 → concatenate along the row dimension
axis=1 → concatenate along the column dimension
```

### Broadcasting

NumPy compares array dimensions from right to left.

Two dimensions are compatible when:

1. They are equal.
2. One of them is `1`.
3. One array has no corresponding dimension.

Incompatible dimensions result in a broadcasting error.

### `flatten()` vs. `ravel()`

```text
flatten() → always returns a copy
ravel()   → returns a view when possible
```

Both return a one-dimensional array.

### `concatenate()` vs. `stack()`

```text
concatenate() → joins arrays along an existing axis
stack()       → joins arrays along a new axis
```

## Applications in Data Science

NumPy supports several common Data Science tasks:

- Numerical data processing
- Statistical calculations
- Array-based transformations
- Efficient mathematical operations
- Matrix operations
- Preparing numerical data for analysis and machine learning

It also provides functionality used by libraries such as **Pandas, Matplotlib, and scikit-learn**.

## Tools and Technologies

- **Language:** Python
- **Library:** NumPy
- **Environment:** Jupyter Notebook

## Notebook

[`numpy_analysis.ipynb`](./numpy_analysis.ipynb)