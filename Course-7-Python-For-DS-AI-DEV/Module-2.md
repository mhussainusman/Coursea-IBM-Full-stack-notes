# Course 7: Python for Data Science, AI & Development

## Module 2: Python Data Structures

### Key Concepts
- Tuples: ordered, immutable collections of elements.
- Lists: ordered, mutable collections of elements.
- Dictionaries: key-value pairs with unique, immutable keys.
- Sets: unordered collections of unique elements.

### Notes
Tuples group related data and are immutable, meaning you cannot change their content after creation. They support indexing, slicing, and concatenation but require creating new tuples for modifications. Lists are similar to tuples but mutable, allowing addition, deletion, and modification of elements. Dictionaries store data as key-value pairs, where keys must be unique and immutable, and values can be mutable or immutable. They allow fast data retrieval by key and support adding or removing pairs. Sets are collections of unique elements without order, useful for removing duplicates and performing mathematical set operations like union and intersection. Understanding these data structures is essential for organizing and manipulating data efficiently in Python.

### Code Examples
```python
# Tuple example
my_tuple = (1, "apple", 3.14)
print(my_tuple[1])  # Access element by index

# List example
my_list = [1, "banana", 2.71]
my_list.append("orange")  # Modify list by adding element
print(my_list)

# Dictionary example
my_dict = {"name": "Alice", "age": 30}
print(my_dict["name"])  # Access value by key
my_dict["age"] = 31  # Modify value

# Set example
my_set = set([1, 2, 2, 3])
my_set.add(4)  # Add element to set
print(my_set)
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| tuple() | Creates an immutable ordered collection |
| list() | Creates a mutable ordered collection |
| dict() | Creates a collection of key-value pairs |
| set() | Creates an unordered collection of unique elements |
| append() | Adds an element to a list |
| keys() | Returns all keys in a dictionary |
| values() | Returns all values in a dictionary |
| & (set operation) | Returns intersection of two sets |
| union() | Combines elements of two sets |

### Glossary
- **Tuple**: An ordered, immutable collection of elements.
- **List**: An ordered, mutable collection of elements.
- **Dictionary**: A collection of key-value pairs with unique keys.
- **Set**: An unordered collection of unique elements.
- **Immutable**: Cannot be changed after creation.
- **Mutable**: Can be changed after creation.

### Summary
This module covers Python's fundamental data structures: tuples, lists, dictionaries, and sets. Each serves different purposes in data organization and manipulation, with varying properties of mutability and ordering. Mastery of these structures is crucial for effective Python programming in data science and development.