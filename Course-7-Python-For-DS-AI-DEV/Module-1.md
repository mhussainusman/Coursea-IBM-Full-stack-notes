# Course 7: Python for Data Science, AI & Development

## Module 1: Python Basics

### Key Concepts
- Python data types: integers, floats, strings, and Booleans.
- Variables and expressions: storing, manipulating data, and performing operations.
- String operations: indexing, slicing, concatenation, immutability, and methods.

### Notes
This module introduces fundamental Python concepts essential for programming. It covers how Python distinguishes between data types such as integers (whole numbers), floats (decimal numbers), strings (text), and Booleans (True/False). You learn how to convert between these types using typecasting. Expressions combine values and operations to produce results, following the order of operations (BODMAS). Variables store data and can be reassigned, allowing dynamic manipulation. String operations include accessing characters by index, slicing with optional stride, concatenating, and replicating strings. Strings are immutable, meaning they cannot be changed after creation, but you can create new strings through operations. Escape sequences help format strings, and Python provides many built-in string methods for searching, modifying, and formatting text.

### Code Examples
```python
# Integer and float typecasting
x = 5          # integer
y = float(x)   # convert to float
z = int(y)     # convert back to integer

# Variable assignment and reassignment
a = 10
a = a + 5      # a is now 15

# String operations
s = "Hello, World!"
print(s[0])    # H (indexing)
print(s[7:12]) # World (slicing)
print(s * 2)   # Hello, World!Hello, World! (replication)
print(len(s))  # 13 (length)

# Using escape sequences
print("Line1\nLine2")  # prints Line1 and Line2 on separate lines

# String methods
print(s.lower())       # hello, world!
print(s.replace("World", "Python"))  # Hello, Python!
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| int() | Converts a value to an integer |
| float() | Converts a value to a float |
| str() | Converts a value to a string |
| = | Assigns a value to a variable |
| // | Integer division (discards fractional part) |
| [] | Access characters in a string by index |
| [:] | Slice a string or sequence |
| * | Replicate a string |
| len() | Returns the length of a string or sequence |
| \n, \t, \\ | Escape sequences for newline, tab, backslash |
| .lower(), .replace() | String methods to change case and replace text |

### Glossary
- **Integer**: A whole number, positive or negative, without decimals.
- **Float**: A number that includes decimals.
- **String**: A sequence of characters enclosed in quotes.
- **Boolean**: A data type with two possible values: True or False.
- **Variable**: A named storage for data that can be changed.
- **Immutable**: Cannot be changed after creation (applies to strings).
- **Typecasting**: Converting a value from one data type to another.
- **Expression**: Combination of values and operations that produces a result.

### Summary
This module lays the foundation for Python programming by teaching data types, variables, expressions, and string operations. Understanding these basics is crucial for writing and manipulating code effectively in Python.