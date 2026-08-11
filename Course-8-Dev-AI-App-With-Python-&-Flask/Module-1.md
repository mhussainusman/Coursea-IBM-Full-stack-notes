# Course 8: Developing AI Applications with Python and Flask

## Module 1: Python Coding Practices and Packaging Concepts

### Key Concepts
- Application development lifecycle phases
- Differences between web apps and APIs
- PEP8 guidelines for code readability and consistency
- Static code analysis and unit testing
- Creating and verifying Python packages

### Notes
The application development lifecycle consists of seven phases: requirement gathering, analysis, design, code and test, user and system test, production, and maintenance. Web applications are a type of API that share data over networks, but not all APIs are web apps. PEP8 guidelines help maintain code readability and consistency by specifying indentation, spacing, naming conventions for functions, classes, and constants. Static code analysis checks code style without execution, while unit testing validates individual code units before integration. To create a Python package, you make a folder with the package name, add an empty __init__.py file, include required modules, and reference them in __init__.py. Verification can be done via a Python shell in the terminal.

### Code Examples
```python
# Example of creating a package structure
mypackage/
    __init__.py
    module1.py
    module2.py

# __init__.py content
from .module1 import *
from .module2 import *
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| Requirement Gathering | Collect user, business, and technical needs |
| PEP8 | Python style guide for readable and consistent code |
| Static Code Analysis | Checks code style without running the code |
| Unit Testing | Tests individual code units for correctness |
| __init__.py | Marks a directory as a Python package |

### Glossary
- **Application Development Lifecycle**: The process of developing software through defined phases from requirements to maintenance.
- **PEP8**: Python Enhancement Proposal 8, a style guide for Python code.
- **Static Code Analysis**: Technique to analyze code for errors and style without executing it.
- **Unit Testing**: Testing individual components of code to ensure they work as expected.
- **Package**: A collection of Python modules organized in a directory with an __init__.py file.

### Summary
This module covers the full application development lifecycle and emphasizes writing clean, consistent Python code following PEP8 guidelines. It introduces static code analysis and unit testing to ensure code quality and reliability. Finally, it explains how to create and verify Python packages for modular and maintainable code.