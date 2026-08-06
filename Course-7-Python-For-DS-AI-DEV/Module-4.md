# Course 7: Python for Data Science, AI & Development

## Module 4: Working with Data in Python

### Key Concepts
- Reading and writing files using Python's open() function with modes 'r', 'w', and 'a'.
- Using the with statement to handle file operations safely.
- Introduction to Pandas for data manipulation with DataFrames and Series.
- Using NumPy for numerical and matrix operations with arrays.
- Vector operations including addition, subtraction, scalar multiplication, Hadamard product, and dot product.
- Accessing and manipulating array attributes like shape, size, and dtype.
- Integration of Matplotlib for data visualization with NumPy arrays.

### Notes
This module covers essential techniques for handling data in Python. You learned how to read from and write to files using the open() function with different modes: 'r' for reading, 'w' for writing (overwriting), and 'a' for appending. The with statement is used to ensure files are properly closed after operations. Pandas, a powerful library for data analysis, was introduced with its DataFrame structure that organizes data in rows and columns, allowing easy manipulation and saving of data. You explored methods to find unique elements and apply Boolean indexing in DataFrames. NumPy, the foundational library for numerical computing in Python, was covered extensively, including creating one- and two-dimensional arrays, accessing elements, and performing vector and matrix operations efficiently. You also learned about array attributes such as shape, size, and data type. The module highlighted the importance of vectorized operations for performance and introduced the Hadamard product and dot product for element-wise and scalar multiplications. Finally, you saw how NumPy arrays can be used with Matplotlib to create visualizations.

### Code Examples
```python
# Reading a file
with open('data.txt', 'r') as file:
    content = file.read()

# Writing to a file
with open('output.txt', 'w') as file:
    file.write("Hello, World!\n")

# Appending to a file
with open('output.txt', 'a') as file:
    file.write("Appending a new line.\n")

# Importing Pandas and reading a CSV file
import pandas as pd
df = pd.read_csv('data.csv')

# Accessing unique values in a column
unique_values = df['column_name'].unique()

# Creating a NumPy array and performing vector addition
import numpy as np
a = np.array([1, 2, 3])
b = np.array([4, 5, 6])
c = a + b  # Vector addition

# Dot product of two arrays
dot_product = np.dot(a, b)

# Multiplying array by scalar
scaled = 3 * a
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| open(filename, mode) | Opens a file with specified mode ('r', 'w', 'a') |
| with open(...) as file: | Context manager to handle file operations safely |
| pd.read_csv() | Reads CSV file into a Pandas DataFrame |
| df['column'].unique() | Returns unique values in a DataFrame column |
| np.array() | Creates a NumPy array |
| np.dot(a, b) | Computes dot product of arrays a and b |
| array.shape | Returns dimensions of a NumPy array |
| array.size | Returns total number of elements in array |
| array.dtype | Returns data type of array elements |

### Glossary
- **open()**: Python function to open files for reading, writing, or appending.
- **with statement**: Ensures proper acquisition and release of resources like files.
- **Pandas DataFrame**: A 2D labeled data structure with columns of potentially different types.
- **NumPy array**: A multidimensional, fixed-size container of elements of the same type optimized for numerical operations.
- **Hadamard product**: Element-wise multiplication of two arrays of the same shape.
- **Dot product**: Sum of the products of corresponding elements of two arrays.

### Summary
This module introduced file handling in Python and key libraries for data science: Pandas and NumPy. You learned how to manipulate data efficiently using DataFrames and arrays, perform vector and matrix operations, and prepare data for analysis and visualization. These skills form the foundation for working with data in Python.