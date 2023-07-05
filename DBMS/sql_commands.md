#### Some of the most used SQL Queries

SELECT - extracts data from a database
UPDATE - updates data in a database
DELETE - deletes data from a database
INSERT INTO - inserts new data into a database
CREATE DATABASE - creates a new database
ALTER DATABASE - modifies a database
CREATE TABLE - creates a new table
ALTER TABLE - modifies a table
DROP TABLE - deletes a table
CREATE INDEX - creates an index (search key)
DROP INDEX - deletes an index

## SQL Basics Documentation

### Table: Employees

| EmployeeID | Name     | Age | Department  |
|------------|----------|-----|-------------|
| 1          | John     | 25  | Marketing   |
| 2          | Sarah    | 28  | Finance     |
| 3          | Michael  | 30  | Operations  |
| 4          | Emily    | 25  | Marketing   |
| 5          | David    | 32  | HR          |
| 6          | Jessica  | 28  | Operations  |
| 7          | Benjamin | 27  | Finance     |
| 8          | Olivia   | 29  | HR          |
| 9          | Ethan    | 26  | Marketing   |
| 10         | Ava      | 31  | HR          |

This documentation will guide you through various SQL topics, providing explanations and examples for each. Let's get started!

### SELECT

The `SELECT` statement is used to retrieve data from a database. It allows you to specify which columns you want to retrieve and from which table. Here's an example that selects all columns from the Employees table:

```sql
SELECT * FROM Employees;
```

Output:

| EmployeeID | Name     | Age | Department  |
|------------|----------|-----|-------------|
| 1          | John     | 25  | Marketing   |
| 2          | Sarah    | 28  | Finance     |
| 3          | Michael  | 30  | Operations  |
| 4          | Emily    | 25  | Marketing   |
| 5          | David    | 32  | HR          |
| 6          | Jessica  | 28  | Operations  |
| 7          | Benjamin | 27  | Finance     |
| 8          | Olivia   | 29  | HR          |
| 9          | Ethan    | 26  | Marketing   |
| 10         | Ava      | 31  | HR          |

### SELECT DISTINCT

The `SELECT DISTINCT` statement is used to retrieve unique values from a column. It eliminates duplicate rows in the result set. Here's an example that selects unique departments from the Employees table:

```sql
SELECT DISTINCT Department FROM Employees;
```

Output:

| Department  |
|-------------|
| Marketing   |
| Finance     |
| Operations  |
| HR          |

### WHERE (Operators)

The `WHERE` clause is used to filter data based on a condition. It allows you to specify criteria to select specific rows from a table. Here's an example that selects employees with an age greater than 28:

```sql
SELECT * FROM Employees WHERE Age > 28;
```

Output:

| EmployeeID | Name     | Age | Department |
|------------|----------|-----|------------|
| 3          | Michael  | 30  | Operations |
| 5          | David    | 32  | HR         |
| 8          | Olivia   | 29  | HR         |
| 10         | Ava      | 31  | HR         |

Common operators used in the WHERE clause include:
- `=` (equals)
- `<>` or `!=` (not equals)
- `>` (greater than)
- `<` (less than)
- `>=` (greater than or equal to)
- `<=` (less than or equal to)

### AND, OR, and NOT

The `AND`, `OR`, and `NOT` operators are used to combine multiple conditions in the WHERE clause.

- `AND`: Retrieves rows that satisfy both conditions.
- `OR`: Retrieves rows that satisfy either condition

- `NOT`: Retrieves rows that do not satisfy a condition.

Here's an example that selects employees who are either in the Marketing department or have an age less than 26:

```sql
SELECT * FROM Employees WHERE Department = 'Marketing' OR Age < 26;
```

Output:

| EmployeeID | Name    | Age | Department |
|------------|---------|-----|------------|
| 1          | John    | 25  | Marketing  |
| 4          | Emily   | 25  | Marketing  |
| 9          | Ethan   | 26  | Marketing  |

### ORDER BY (ASC and DESC)

The `ORDER BY` clause is used to sort the result set based on one or more columns. By default, it sorts in ascending order (`ASC`). You can also specify descending order (`DESC`). Here's an example that retrieves employees sorted by age in descending order:

```sql
SELECT * FROM Employees ORDER BY Age DESC;
```

Output:

| EmployeeID | Name     | Age | Department  |
|------------|----------|-----|-------------|
| 5          | David    | 32  | HR          |
| 10         | Ava      | 31  | HR          |
| 3          | Michael  | 30  | Operations  |
| 8          | Olivia   | 29  | HR          |
| 6          | Jessica  | 28  | Operations  |
| 2          | Sarah    | 28  | Finance     |
| 7          | Benjamin | 27  | Finance     |
| 9          | Ethan    | 26  | Marketing   |
| 1          | John     | 25  | Marketing   |
| 4          | Emily    | 25  | Marketing   |

### INSERT INTO

The `INSERT INTO` statement is used to insert new rows into a table. You need to specify the table name and the values for each column. Here's an example that inserts a new employee into the Employees table:

```sql
INSERT INTO Employees (EmployeeID, Name, Age, Department) 
VALUES (11, 'Sophia', 24, 'Finance');
```

After executing the above statement, the Employees table will have a new row:

| EmployeeID | Name     | Age | Department  |
|------------|----------|-----|-------------|
| ...        | ...      | ... | ...         |
| 11         | Sophia   | 24  | Finance     |

### NULL Value

The `NULL` value represents missing or unknown data. It is used when a value is not applicable or not known at the time of data entry. Here's an example that retrieves employees with a null value in the Department column:

```sql
SELECT * FROM Employees WHERE Department IS NULL;
```

Output: (assuming there are no null values in the Department column)

| EmployeeID | Name     | Age | Department  |
|------------|----------|-----|-------------|
| ...        | ...      | ... | ...         |

To insert a NULL value, you can omit the value or use the keyword `NULL` in the `INSERT INTO` statement:

```sql
INSERT INTO Employees (EmployeeID, Name, Age, Department) 
VALUES (12, 'Jacob', 27, NULL);
```

### UPDATE

The `UPDATE` statement is used to modify existing rows in a table. You can update one or more columns based on a condition. Here's an example that updates the department of an employee:

```sql
UPDATE Employees SET Department = 'Operations' WHERE EmployeeID = 2;
```

After executing the above statement, the Employees table will be updated:

| EmployeeID | Name     | Age |

Department  |
|------------|----------|-----|-------------|
| 1          | John     | 25  | Marketing   |
| 2          | Sarah    | 28  | Operations  |
| 3          | Michael  | 30  | Operations  |
| ...        | ...      | ... | ...         |

### DELETE

The `DELETE` statement is used to delete existing rows from a table based on a condition. Here's an example that deletes an employee from the Employees table:

```sql
DELETE FROM Employees WHERE EmployeeID = 4;
```

After executing the above statement, the Employees table will have the employee with EmployeeID 4 removed:

| EmployeeID | Name     | Age | Department  |
|------------|----------|-----|-------------|
| 1          | John     | 25  | Marketing   |
| 2          | Sarah    | 28  | Operations  |
| 3          | Michael  | 30  | Operations  |
| ...        | ...      | ... | ...         |

### MIN() and MAX()

The `MIN()` and `MAX()` functions are used to retrieve the minimum and maximum values from a column, respectively. Here's an example that retrieves the minimum and maximum ages from the Employees table:

```sql
SELECT MIN(Age) AS MinAge, MAX(Age) AS MaxAge FROM Employees;
```

Output:

| MinAge | MaxAge |
|--------|--------|
| 25     | 32     |

### COUNT(), AVG(), and SUM()

The `COUNT()`, `AVG()`, and `SUM()` functions are used to perform calculations on a column.

- `COUNT()` returns the number of rows that match the specified condition.
- `AVG()` returns the average value of a numeric column.
- `SUM()` returns the sum of values in a numeric column.

Here's an example that retrieves the count, average age, and total age of employees:

```sql
SELECT COUNT(*) AS TotalEmployees, AVG(Age) AS AvgAge, SUM(Age) AS TotalAge FROM Employees;
```

Output:

| TotalEmployees | AvgAge | TotalAge |
|----------------|--------|----------|
| 10             | 28.1   | 281      |

### BETWEEN

The `BETWEEN` operator is used to retrieve values within a specified range. It is inclusive of the endpoints. Here's an example that retrieves employees with ages between 25 and 30:

```sql
SELECT * FROM Employees WHERE Age BETWEEN 25 AND 30;
```

Output:

| EmployeeID | Name     | Age | Department  |
|------------|----------|-----|-------------|
| 1          | John     | 25  | Marketing   |
| 2          | Sarah    | 28  | Operations  |
| 3          | Michael  | 30  | Operations  |
| 4          | Emily    | 25  | Marketing   |
| 9          | Ethan    | 26  | Marketing   |
| 8          | Olivia   | 29  | HR          |
| ...        | ...      | ... | ...         |

### INNER JOIN

The `INNER JOIN` combines rows from two or more tables based on a related column. It retrieves rows that have matching values in both tables. Here's an example that retrieves employees along with their corresponding departments:

```sql
SELECT Employees.Name, Employees.Age, Departments.DepartmentName
FROM Employees
INNER JOIN Departments ON Employees.DepartmentID = Departments.DepartmentID;
```

Assuming there is a Departments table with DepartmentID and DepartmentName columns, the output would be:

| Name     | Age | DepartmentName |
|----------|-----|----------------|
| John

| 25  | Marketing      |
| Sarah    | 28  | Finance        |
| Michael  | 30  | Operations     |
| Emily    | 25  | Marketing      |
| David    | 32  | HR             |
| Jessica  | 28  | Operations     |
| Benjamin | 27  | Finance        |
| Olivia   | 29  | HR             |
| Ethan    | 26  | Marketing      |
| Ava      | 31  | HR             |

### LEFT JOIN

The `LEFT JOIN` retrieves all rows from the left table and the matching rows from the right table. If there is no match, NULL values are returned for the columns of the right table. Here's an example that retrieves all employees and their corresponding departments, including employees without departments:

```sql
SELECT Employees.Name, Employees.Age, Departments.DepartmentName
FROM Employees
LEFT JOIN Departments ON Employees.DepartmentID = Departments.DepartmentID;
```

Output:

| Name     | Age | DepartmentName |
|----------|-----|----------------|
| John     | 25  | Marketing      |
| Sarah    | 28  | Finance        |
| Michael  | 30  | Operations     |
| Emily    | 25  | Marketing      |
| David    | 32  | HR             |
| Jessica  | 28  | Operations     |
| Benjamin | 27  | Finance        |
| Olivia   | 29  | HR             |
| Ethan    | 26  | Marketing      |
| Ava      | 31  | HR             |

### RIGHT JOIN

The `RIGHT JOIN` retrieves all rows from the right table and the matching rows from the left table. If there is no match, NULL values are returned for the columns of the left table. Here's an example that retrieves all departments and the employees associated with them, including departments without employees:

```sql
SELECT Employees.Name, Employees.Age, Departments.DepartmentName
FROM Employees
RIGHT JOIN Departments ON Employees.DepartmentID = Departments.DepartmentID;
```

Output:

| Name     | Age | DepartmentName |
|----------|-----|----------------|
| John     | 25  | Marketing      |
| Sarah    | 28  | Finance        |
| Michael  | 30  | Operations     |
| Emily    | 25  | Marketing      |
| David    | 32  | HR             |
| Jessica  | 28  | Operations     |
| Benjamin | 27  | Finance        |
| Olivia   | 29  | HR             |
| Ethan    | 26  | Marketing      |
| Ava      | 31  | HR             |
| NULL     | NULL| Sales          |

### FULL JOIN

The `FULL JOIN` retrieves all rows from both the left and right tables. If there is no match, NULL values are returned for the columns of the non-matching table. Here's an example that retrieves all employees and departments, including those without matches:

```sql
SELECT Employees.Name, Employees.Age, Departments.DepartmentName
FROM Employees
FULL JOIN Departments ON Employees.DepartmentID = Departments.DepartmentID;
```

Output:

| Name     | Age | DepartmentName |
|----------|-----|----------------|
| John     | 25  | Marketing      |
| Sarah    | 28  | Finance        |
| Michael  | 30  | Operations     |
| Emily    | 25  | Marketing      |
| David    | 32  | HR             |
| Jessica  | 28  | Operations     |
| Benjamin | 27  | Finance        |
| Olivia   | 29  | HR             |
| Ethan    | 26  | Marketing      |
| Ava      | 31  | HR            

### UNION

The `UNION` operator is used to combine the result sets of two or more SELECT statements into a single result set. The columns in the SELECT statements must have the same data types and be in the same order. Here's an example that retrieves employees from both the Marketing and HR departments:

```sql
SELECT Name, Age, Department
FROM Employees
WHERE Department = 'Marketing'
UNION
SELECT Name, Age, Department
FROM Employees
WHERE Department = 'HR';
```

Output:

| Name     | Age | Department |
|----------|-----|------------|
| John     | 25  | Marketing  |
| Emily    | 25  | Marketing  |
| Ethan    | 26  | Marketing  |
| David    | 32  | HR         |
| Olivia   | 29  | HR         |
| Ava      | 31  | HR         |

### GROUP BY

The `GROUP BY` clause is used to group rows based on one or more columns. It is often used with aggregate functions to perform calculations on each group. Here's an example that calculates the count of employees in each department:

```sql
SELECT Department, COUNT(*) AS EmployeeCount
FROM Employees
GROUP BY Department;
```

Output:

| Department | EmployeeCount |
|------------|---------------|
| Marketing  | 4             |
| Finance    | 2             |
| Operations | 2             |
| HR         | 3             |

In this documentation, we covered various SQL topics, including SELECT, SELECT DISTINCT, WHERE (Operators), AND/OR/NOT, ORDER BY (ASC and DESC), INSERT INTO, NULL Value, UPDATE, DELETE, MIN() and MAX(), COUNT(), AVG(), and SUM(), BETWEEN, INNER JOIN, LEFT JOIN, RIGHT JOIN, FULL JOIN, UNION, and GROUP BY. These concepts and examples provide a solid foundation for working with SQL and retrieving, manipulating, and analyzing data from relational databases.