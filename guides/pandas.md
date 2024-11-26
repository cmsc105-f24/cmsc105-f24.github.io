---
layout: default  
permalink: /guides/pandas  
title: Pandas Guide  
---

# Pandas Guide

Here are some essential functions and methods in Pandas for working with data in Python. For a full reference, refer to the official Pandas documentation: [Pandas Documentation](https://pandas.pydata.org/docs/).

Before you begin, make sure to import Pandas at the start of your script:

```python
import pandas as pd
```

## Creating DataFrames and Series

- **`pd.DataFrame(data, columns=None, index=None)`**:
   - **Description**: Creates a DataFrame from a dictionary, list, or other data structure.
   - **Parameters**:
     - `data`: The input data (e.g., dictionary, 2D list, or NumPy array).
     - `columns` (optional): List of column names.
     - `index` (optional): List of row labels.
   - **Example**:
     ```python
     data = {'Name': ['Alice', 'Bob'], 'Age': [25, 30]}
     df = pd.DataFrame(data)
     print(df)
     # Outputs:
     #     Name  Age
     # 0  Alice   25
     # 1    Bob   30
     ```

- **`pd.Series(data, index=None)`**:
   - **Description**: Creates a Series, which is a one-dimensional labeled array.
   - **Parameters**:
     - `data`: Input data (e.g., list, dictionary, or scalar value).
     - `index` (optional): List of labels for the Series.
   - **Example**:
     ```python
     series = pd.Series([1, 2, 3], index=['a', 'b', 'c'])
     print(series)
     # Outputs:
     # a    1
     # b    2
     # c    3
     ```

## Basic Operations

- **`df.head(n)`**:
   - **Description**: Returns the first `n` rows of the DataFrame (default is 5).
   - **Example**:
     ```python
     df = pd.DataFrame({'A': range(10)})
     print(df.head(3))
     # Outputs:
     #    A
     # 0  0
     # 1  1
     # 2  2
     ```

- **`df.tail(n)`**:
   - **Description**: Returns the last `n` rows of the DataFrame (default is 5).
   - **Example**:
     ```python
     print(df.tail(3))
     # Outputs:
     #    A
     # 7  7
     # 8  8
     # 9  9
     ```

- **`df.describe()`**:
   - **Description**: Provides summary statistics of numeric columns.
   - **Example**:
     ```python
     df = pd.DataFrame({'A': [1, 2, 3], 'B': [4, 5, 6]})
     print(df.describe())
     # Outputs:
     #          A    B
     # count  3.0  3.0
     # mean   2.0  5.0
     # std    1.0  1.0
     # min    1.0  4.0
     # 25%    1.5  4.5
     # 50%    2.0  5.0
     # 75%    2.5  5.5
     # max    3.0  6.0
     ```

## Data Selection and Manipulation

- **`df['column']` or `df[column]`**:
   - **Description**: Selects a column as a Series.
   - **Example**:
     ```python
     print(df['A'])
     # Outputs:
     # 0    1
     # 1    2
     # 2    3
     ```

- **`df.loc[row_labels, col_labels]`**:
   - **Description**: Accesses rows and columns by labels.
   - **Example**:
     ```python
     df = pd.DataFrame({'A': [1, 2], 'B': [3, 4]}, index=['x', 'y'])
     print(df.loc['x', 'A'])
     # Outputs: 1
     ```

- **`df.iloc[row_index, col_index]`**:
   - **Description**: Accesses rows and columns by integer indices.
   - **Example**:
     ```python
     print(df.iloc[0, 1])
     # Outputs: 3
     ```

- **`df.drop(labels, axis)`**:
   - **Description**: Removes rows or columns by labels.
   - **Parameters**:
     - `labels`: Name or index of the row(s) or column(s) to drop.
     - `axis`: 0 for rows, 1 for columns.
   - **Example**:
     ```python
     df = df.drop('B', axis=1)
     print(df)
     # Outputs:
     #    A
     # x  1
     # y  2
     ```

## Grouping and Aggregations

- **`df.groupby(by)`**:
   - **Description**: Groups the data by the specified column(s) for aggregation.
   - **Parameters**:
     - `by`: Column(s) to group by.
   - **Example**:
     ```python
     df = pd.DataFrame({'Category': ['A', 'A', 'B'], 'Value': [10, 20, 30]})
     print(df.groupby('Category').sum())
     # Outputs:
     #           Value
     # Category       
     # A            30
     # B            30
     ```

For more advanced features, check out the official Pandas [Documentation](https://pandas.pydata.org/docs/).
