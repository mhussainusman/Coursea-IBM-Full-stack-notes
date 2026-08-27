# Course 9: Django Application Development with SQL and Databases

## Module 1: Getting Started with SQL & Relational Databases

### Key Concepts
- SQL (Structured Query Language) is used for querying and managing structured data in relational databases.
- The SELECT statement retrieves data from tables.
- The INSERT statement adds new rows to tables.
- The UPDATE statement modifies existing data.
- The DELETE statement removes data from tables.
- The WHERE clause filters rows affected by SELECT, UPDATE, or DELETE.

### Notes
SQL is a powerful language designed to work with relational databases, which organize data into tables with rows and columns. The SELECT statement is used to query and retrieve data, producing a result set. INSERT adds new data rows, requiring the number of values to match the specified columns. UPDATE changes existing data based on conditions, and DELETE removes data rows selectively. The WHERE clause is essential for targeting specific rows in these operations.

### Code Examples
```sql
-- Select all columns from a table
SELECT * FROM TableName;

-- Insert a new row into a table
INSERT INTO TableName (Column1, Column2) VALUES (Value1, Value2);

-- Update rows in a table
UPDATE TableName SET Column1 = NewValue WHERE Condition;

-- Delete rows from a table
DELETE FROM TableName WHERE Condition;
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| SELECT | Retrieves data from a table |
| INSERT INTO | Adds new rows to a table |
| UPDATE | Modifies existing data in a table |
| DELETE FROM | Removes data from a table |
| WHERE | Filters rows for SELECT, UPDATE, DELETE |

### Glossary
- **SQL**: Structured Query Language used to manage and query relational databases.
- **Result Set**: The output table returned by a SELECT query.
- **WHERE clause**: A condition to specify which rows are affected by a query.

### Summary
This module introduces SQL basics for managing data in relational databases. You learned how to retrieve, insert, update, and delete data using SQL statements, with the WHERE clause to target specific rows. These fundamentals are essential for working with databases in application development.