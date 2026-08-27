# Course 9: Django Application Development with SQL and Databases

## Module 2: ORM: Bridging the Gap Between the Real World and Relational Model

### Key Concepts
- Object-Oriented Programming (OOP) and SQL model data differently.
- Object Relational Mapping (ORM) bridges the gap between OOP and SQL.
- ORM tools map data between relational database rows and objects.
- Django ORM is a Python ORM that integrates with the Django framework.
- Django ORM supports CRUD operations through model APIs.

### Notes
ORM allows developers to work with databases using object-oriented programming by converting objects into database rows and vice versa. This abstraction simplifies database interactions by letting developers manipulate data as objects rather than writing raw SQL queries. Django ORM automates table creation based on defined models and fields, mapping each model to a database table and each field to a column. CRUD operations—Create, Read, Update, Delete—are performed using Django model methods and QuerySets, making database management more intuitive and integrated within Python code.

### Code Examples
```python
# Create and save a new object
obj = MyModel(field1='value1', field2='value2')
obj.save()

# Read objects using QuerySet
objects = MyModel.objects.filter(field1='value1')

# Update an object
obj.field2 = 'new_value'
obj.save()

# Delete an object
obj.delete()
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| save() | Inserts or updates a model object in the database |
| objects.filter() | Retrieves objects matching given criteria |
| delete() | Deletes a model object or queryset from the database |
| QuerySet | A collection of database objects returned by a query |

### Glossary
- **ORM (Object Relational Mapping)**: A technique that maps objects in code to rows in a relational database.
- **Django Model**: A Python class that defines the structure of a database table.
- **QuerySet**: A Django object representing a collection of database records.

### Summary
This module explains how ORM bridges the conceptual gap between object-oriented programming and relational databases. Django ORM enables developers to interact with databases using Python objects, simplifying CRUD operations and speeding up development by automating table creation and data manipulation.