### 1. What is Primary Key?
- A primary key is a unique identifier for each record in a table. No two rows can have the same primary key value, and it cannot be NULL.
```sql
CREATE TABLE students (
    student_id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT
);
```
### 2. What is foreign key ?
- A Foreign Key is a column in one table that refers to the Primary Key of another table. It is used to maintain relationships between tables.
```sql
CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    order_date DATE,
    customer_id INT,
    FOREIGN KEY (customer_id) REFERENCES customers(customer_id)
);
```

### 3. Explain distinct command in SQL.
- DISTINCT removes duplicate values from the result set.
```sql
SELECT DISTINCT city FROM customers;
```
- This returns unique city names only.

### 4. How do you find a particular character or element in a string
- Using **in** operator
```python
"a" in "mango"   # True
```
- Using **find**
```python
"mango".find("g")   # returns index 2
```
- Using **index**
```python
"apple".index("p")  # returns index 1
```
- count occurences
```python
"banana".count("a")  # 3
```
### 5. What is composite key?
- A Composite Key is a Primary Key made from two or more columns together. Used when single column cannot uniquely identify a row. 
```sql
PRIMARY KEY (student_id, course_id)
```
### 6. When you will use SQL and NoSQL
**Use of SQL (Relational Databases):**
- Data is structured
- Need relationships (foreign keys)
- Require ACID transactions
- Examples: Banking, ecommerce orders

**Use of NoSQL:**
- Data is unstructured or semi-structured
- Need high speed, high scalability
- Flexible schema
- Examples: Social media feeds, logs, big data apps
### 7. Tell me any four aggregate functions in SQL.
1. Count(): Count number of rows.
```sql
SELECT COUNT(*) AS total_customers
FROM customers;
```

2. Add(): Add all numeric values
```sql
SELECT SUM(salary) AS total_salary
FROM employees;
```

3. Avg(): Calculate average value
```sql
SELECT AVG(marks) AS average_marks
FROM students;
```

4. Fetch(): Fetch highest value
```sql
SELECT MAX(salary) AS highest_salary
FROM employees;
```

### 8. Tell me the command for creating a new user with password
```sql
CREATE ROLE jahnavi WITH LOGIN PASSWORD 'password123';
```
### 9. What is foreign key ?
- A Foreign Key is a column in one table that refers to the Primary Key of another table. It is used to maintain relationships between tables.

```sql
CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    order_date DATE,
    customer_id INT,
    FOREIGN KEY (customer_id) REFERENCES customers(customer_id)
);
```
### 10. What is the use of DROP keyword  in SQL.
- DROP is used to permanently delete a database object such as:

- table
- database
- column
- user
- view
```sql
DROP TABLE employees;
```
### 11. What are constraints in SQL ?
- Constraints are rules applied to columns to maintain data accuracy and integrity.
- Common constraints:
1. PRIMARY KEY
2. FOREIGN KEY
3. UNIQUE
4. NOT NULL
5. CHECK
6. DEFAULT

### 12. How subquery is useful in SQL.
- A subquery is a query inside another query. It is used to filter, compare, or compute values using results from another query.
- Example:
```sql
SELECT name
FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);
```