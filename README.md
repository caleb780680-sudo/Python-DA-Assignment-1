# 🐍 Python Data Analytics Assignment 1

## 📌 Project Overview

This project demonstrates fundamental **Python Data Analytics** concepts using **NumPy** and **Pandas**.

The assignment is divided into three parts:

1. **NumPy Array Operations**
2. **Pandas Series**
3. **Pandas DataFrame**

The exercises focus on creating, inspecting, slicing, filtering, manipulating, and analyzing structured data.

---

## 🎯 Objectives

The main objectives of this assignment are to practice:

* Creating NumPy arrays
* Understanding array properties
* Performing numerical calculations
* Indexing and slicing arrays
* Creating Pandas Series
* Manipulating Series data
* Creating Pandas DataFrames
* Exploring datasets
* Filtering data
* Grouping and aggregating data
* Updating and deleting records
* Creating calculated columns

---

# 🔢 Part 1: NumPy Array Operations

The first part works with temperature data using NumPy.

### 📊 1D Array

A one-dimensional array containing weekly temperature values is created:

```python
temperatures_w1 = np.array([
    22.5, 25.3, 20.8, 23.4,
    26.1, 24.8, 21.9
])
```

### 🔍 Array Inspection

The following properties are explored:

* `shape`
* `dtype`
* `size`

### 🌡️ Array Calculations

The assignment performs:

* Celsius-to-Fahrenheit conversion
* Maximum temperature
* Minimum temperature
* Mean temperature

Example:

```python
temperatures_fahrenheit = (temperatures_w1 * 9/5) + 32
```

### ✂️ Indexing & Slicing

The notebook demonstrates:

* First 3 days
* Weekend temperatures
* Middle 3 days

Example:

```python
temperatures_w1[:3]
temperatures_w1[-2:]
temperatures_w1[2:5]
```

### 📅 2D NumPy Array

Temperature data for two weeks is stored in a two-dimensional array.

The assignment explores:

* 2D shape
* Data type
* Total number of elements
* Individual weeks
* Weekend temperatures for each week

---

# 🐼 Part 2: Pandas Series

The second part introduces **Pandas Series** using student marks.

### 📚 Creating a Series

```python
marks = pd.Series(
    [95, 92, 89, 85, 80],
    index=['Rank1', 'Rank2', 'Rank3', 'Rank4', 'Rank5']
)
```

### 🔎 Series Indexing & Slicing

The notebook demonstrates:

* Accessing the first-ranked mark
* Selecting the top 3 ranks
* Accessing a specific rank
* Filtering marks greater than 90

Example:

```python
marks[marks > 90]
```

### ✏️ Series Manipulation

The assignment also demonstrates:

* Updating a value
* Removing an index
* Creating a CGPA calculation

```python
marks.loc['Rank1'] = 100
marks = marks.drop('Rank5')
cgpa = marks / 10
```

---

# 📊 Part 3: Pandas DataFrame

The third part uses a transaction dataset containing:

* Transaction ID
* Product Category
* Region
* Amount

### 🗃️ Dataset Structure

Example columns:

| Column            | Description                   |
| ----------------- | ----------------------------- |
| `TransactionID`   | Unique transaction identifier |
| `ProductCategory` | Category of product           |
| `Region`          | Transaction region            |
| `Amount`          | Transaction amount            |

### 🔍 Data Exploration

The following Pandas operations are practiced:

* `head()`
* `tail()`
* `shape`
* `columns`
* `dtypes`
* Column selection
* `.iloc[]`
* Conditional filtering
* `value_counts()`
* `unique()`
* `groupby()`

Example:

```python
transactions[
    (transactions['Region'] == 'North') &
    (transactions['Amount'] > 200)
]
```

### 📈 Grouping & Aggregation

The assignment calculates the average transaction amount by region:

```python
transactions.groupby('Region')['Amount'].mean()
```

### ✏️ Data Manipulation

The DataFrame is modified by:

* Updating a transaction amount
* Creating a `Discount` column
* Removing a transaction
* Dropping the calculated column

Example:

```python
transactions['Discount'] = transactions['Amount'] * 0.10
```

---

# 🛠️ Technologies Used

* **Python 3**
* **NumPy**
* **Pandas**
* **Jupyter Notebook**

---

# 📚 Concepts Covered

### NumPy

* 1D arrays
* 2D arrays
* Array properties
* Mathematical operations
* Indexing
* Slicing
* Aggregation functions

### Pandas Series

* Series creation
* Custom indexes
* `.iloc[]`
* `.loc[]`
* Filtering
* Updating values
* Dropping values
* Calculated Series

### Pandas DataFrame

* DataFrame creation
* Data exploration
* Column selection
* Row filtering
* `value_counts()`
* `unique()`
* `groupby()`
* Mean calculation
* Updating records
* Adding columns
* Removing records
* Dropping columns

---

# 🎯 Key Learning Outcomes

Through this assignment, I practiced how to:

* Work with numerical data using NumPy
* Analyze arrays efficiently
* Perform indexing and slicing
* Work with one-dimensional Pandas data
* Explore tabular datasets
* Filter data based on conditions
* Calculate grouped statistics
* Modify existing datasets
* Create calculated columns
* Prepare data for further analytics

---

# 📂 Project Structure

```text
Python-DA-Assignment-1/
│
├── Python DA Assighment 1.ipynb
└── README.md
```

---

# 🚀 How to Run

1. Install **Python 3**.
2. Install Jupyter Notebook.
3. Install the required libraries:

```bash
pip install numpy pandas jupyter
```

4. Open the notebook:

```bash
jupyter notebook
```

5. Open `Python DA Assighment 1.ipynb`.
6. Run the cells sequentially.

---

# 💻 Libraries Used

```python
import numpy as np
import pandas as pd
```

---

## 👤 Author

**Caleb**

### ⭐ Python Data Analytics Assignment 1

*NumPy & Pandas Data Analysis Practice*
