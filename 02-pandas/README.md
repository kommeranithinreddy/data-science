# Pandas — Data Manipulation & Analysis

Practical work with **Pandas** for data manipulation, cleaning, transformation, aggregation, and analysis.

This section covers techniques for working with real-world tabular datasets, preparing data for analysis, and extracting meaningful insights using Python.

## Topics Covered

### 1. Data Structures and Inspection

- Series and DataFrames
- Creating Series and DataFrames
- Understanding `shape`, `columns`, `index`, and `dtypes`
- Inspecting datasets with `info()` and `describe()`
- Understanding dataset structure and data types
- Initial data inspection and quality checks

### 2. Selecting and Filtering Data

- Selecting individual and multiple columns
- Label-based selection with `loc`
- Position-based selection with `iloc`
- Boolean filtering
- Multiple filtering conditions
- Combining conditions with `&`, `|`, and `~`
- Selecting rows and columns based on conditions

### 3. Data Cleaning and Modification

- Creating and modifying columns
- Vectorized operations
- Conditional column creation
- Conditional selection with `np.where()`
- Removing rows and columns
- Sorting data
- Detecting and removing duplicates
- Identifying missing values
- Handling missing data with `isna()`, `dropna()`, and `fillna()`
- Data type conversion

### 4. Loading and Saving Data

- Reading CSV files with `read_csv()`
- Reading Excel files with `read_excel()`
- Reading JSON files with `read_json()`
- Working with file paths
- Exporting datasets using `to_csv()`, `to_excel()`, and `to_json()`
- Loading and processing external datasets

### 5. Grouping and Aggregation

- Grouping data with `groupby()`
- Frequency analysis with `value_counts()`
- Aggregation using `sum()`, `mean()`, `min()`, `max()`, `count()`, and `size()`
- Multiple aggregations with `agg()`
- Grouping by multiple columns
- Filtering, grouping, and aggregation
- Sorting grouped results
- Restructuring results with `reset_index()`

### 6. Combining and Transforming Data

- Combining datasets with `merge()` and `concat()`
- Inner, left, right, and outer joins
- Mapping values with `map()`
- Applying custom transformations with `apply()`
- Vectorized transformations
- Combining datasets using common keys

### 7. Text, Dates, and Practical Cleaning

- String operations using the `.str` accessor
- Removing whitespace with `str.strip()`
- Changing text case with `str.lower()`, `str.upper()`, and `str.title()`
- Searching text with `str.contains()`
- Replacing text with `str.replace()`
- Converting values to datetime using `pd.to_datetime()`
- Handling mixed date formats
- Using `format="mixed"` and `errors="coerce"` where appropriate
- Extracting date components with the `.dt` accessor
- Extracting year, month, day, and day names
- Calculating date differences
- Practical text and date cleaning

### 8. Integrated Data Analysis Workflow

Applying Pandas operations together to prepare and analyze a dataset.

```text
Load
  ↓
Inspect
  ↓
Check Data Quality
  ↓
Clean
  ↓
Transform
  ↓
Create Features
  ↓
Filter
  ↓
Group and Aggregate
  ↓
Analyze
  ↓
Interpret Results
```

## Key Concepts

### Pandas and NumPy

| NumPy | Pandas |
|---|---|
| Numerical arrays | Labeled tabular data |
| Mathematical computation | Data manipulation |
| Array operations | Row and column selection |
| Numerical aggregation | Grouping and aggregation |
| Matrix operations | DataFrame operations |
| Numerical processing | Missing-value handling |
| | Text and datetime operations |
| | Combining datasets |

Pandas builds on concepts used in NumPy and provides additional functionality for structured, labeled data.

### Core Pandas Operations

| Operation | Purpose |
|---|---|
| `Series` | Represent one-dimensional labeled data |
| `DataFrame` | Represent two-dimensional tabular data |
| `loc` | Select data using labels |
| `iloc` | Select data using integer positions |
| `merge()` | Join related datasets |
| `concat()` | Combine datasets along an axis |
| `map()` | Map values using a mapping or function |
| `apply()` | Apply a function along an axis |
| `groupby()` | Group data for analysis |
| `.str` | Perform string operations |
| `.dt` | Access datetime components and operations |

### Common Analytical Pattern

A frequently used data analysis pattern is:

```text
FILTER
   ↓
GROUP
   ↓
AGGREGATE
   ↓
INTERPRET
```

Example:

```python
sales[
    sales["Category"] == "Electronics"
].groupby("City")["Sales"].sum()
```

This operation filters Electronics sales, groups the records by city, and calculates the total sales for each city.

## Applications in Data Science

Pandas is used for:

- Loading and inspecting datasets
- Cleaning inconsistent and incomplete data
- Transforming variables and creating features
- Filtering records based on analytical conditions
- Combining data from multiple sources
- Grouping and summarizing observations
- Preparing datasets for Exploratory Data Analysis
- Preparing structured data for machine learning workflows

## Tools and Technologies

- **Language:** Python
- **Libraries:** Pandas, NumPy
- **Environment:** Jupyter Notebook

## Notebook

[`pandas_analysis.ipynb`](./pandas_analysis.ipynb)