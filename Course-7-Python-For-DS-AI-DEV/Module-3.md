# Course 7: Python for Data Science, AI & Development

## Module 3: Python Programming Fundamentals

### Key Concepts
- Python conditions and branching using if, else, and elif statements
- Loops: for and while loops for iteration
- Functions: defining, calling, parameters, return values, and documentation
- Variable scope: local vs global variables
- Exception handling with try-except-else-finally
- Object-oriented programming basics: classes, objects, methods, and attributes

### Notes
This module covers fundamental programming concepts in Python that control the flow of execution and enable code reuse. Conditions and branching allow programs to make decisions based on Boolean expressions, using if, else, and elif to execute different code blocks. Loops automate repetitive tasks by iterating over sequences or running while a condition is true. Functions encapsulate reusable code blocks, improving modularity and clarity; they can take parameters and return results. Understanding variable scope is crucial to managing data access and modification within functions or globally. Exception handling ensures programs can gracefully manage errors without crashing, using try-except blocks and optional else and finally clauses. Finally, the module introduces object-oriented programming, where classes serve as blueprints for creating objects that combine data attributes and methods, enabling organized and scalable code design.

### Code Examples
```python
# Example of if-elif-else branching
x = 10
if x > 0:
    print("Positive number")
elif x == 0:
    print("Zero")
else:
    print("Negative number")

# Example of a for loop iterating over a list
fruits = ["apple", "banana", "cherry"]
for fruit in fruits:
    print(fruit)

# Example of a function with parameters and return value
def add(a, b):
    """Return the sum of a and b."""
    return a + b

result = add(5, 3)
print(result)  # Output: 8

# Example of exception handling
try:
    value = int(input("Enter a number: "))
    print("You entered:", value)
except ValueError:
    print("That's not a valid number!")

# Example of a simple class with attributes and methods
class Dog:
    def __init__(self, name):
        self.name = name

    def bark(self):
        print(f"{self.name} says woof!")

my_dog = Dog("Buddy")
my_dog.bark()
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| if, elif, else | Conditional branching based on Boolean expressions |
| for loop | Iterates over a sequence (list, tuple, string) |
| while loop | Repeats as long as a condition is true |
| def | Defines a function |
| return | Returns a value from a function |
| try-except | Handles exceptions to prevent program crashes |
| class | Defines a blueprint for creating objects |
| __init__ | Special method to initialize object attributes |
| self | Refers to the instance of the class |

### Glossary
- **Boolean expression**: An expression that evaluates to True or False.
- **Function**: A reusable block of code that performs a specific task.
- **Exception**: An error that occurs during program execution.
- **Class**: A blueprint for creating objects with attributes and methods.
- **Object**: An instance of a class containing data and behavior.

### Summary
This module introduces essential Python programming concepts including conditional statements, loops, functions, exception handling, and object-oriented programming. Mastery of these fundamentals enables writing clear, efficient, and robust Python code for a variety of applications.