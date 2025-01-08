# SQL Joins

## Introduction

SQL joins are used to combine rows from two or more tables based on a related column between them. Joins are essential for querying data from multiple tables in a relational database.

## Types of Joins

### Inner Join

An inner join returns only the rows that have matching values in both tables.

### Example

```sql
SELECT users.name, orders.order_date
FROM users
INNER JOIN orders ON users.id = orders.user_id;
```

### Left Join (Left Outer Join)

A left join returns all the rows from the left table and the matching rows from the right table. If there is no match, the result is NULL on the right side.

### Example

```sql
SELECT users.name, orders.order_date
FROM users
LEFT JOIN orders ON users.id = orders.user_id;
```

### Right Join (Right Outer Join)

A right join returns all the rows from the right table and the matching rows from the left table. If there is no match, the result is NULL on the left side.

### Example

```sql
SELECT users.name, orders.order_date
FROM users
RIGHT JOIN orders ON users.id = orders.user_id;
```

### Full Join (Full Outer Join)

A full join returns all the rows when there is a match in either the left or right table. If there is no match, the result is NULL on both sides.

### Example

```sql
SELECT users.name, orders.order_date
FROM users
FULL JOIN orders ON users.id = orders.user_id;
```

### Cross Join

A cross join returns the Cartesian product of the two tables, meaning it returns all possible combinations of rows.

### Example

```sql
SELECT users.name, orders.order_date
FROM users
CROSS JOIN orders;
```

## Example

Combining different types of joins to query data from multiple tables.

```sql
-- Create tables
CREATE TABLE users (
  id INT PRIMARY KEY,
  name VARCHAR(100)
);

CREATE TABLE orders (
  id INT PRIMARY KEY,
  user_id INT,
  order_date DATE,
  FOREIGN KEY (user_id) REFERENCES users(id)
);

-- Insert data into tables
INSERT INTO users (id, name) VALUES (1, 'John Doe');
INSERT INTO users (id, name) VALUES (2, 'Jane Smith');
INSERT INTO orders (id, user_id, order_date) VALUES (1, 1, '2023-01-01');
INSERT INTO orders (id, user_id, order_date) VALUES (2, 2, '2023-01-02');

-- Inner join
SELECT users.name, orders.order_date
FROM users
INNER JOIN orders ON users.id = orders.user_id;

-- Left join
SELECT users.name, orders.order_date
FROM users
LEFT JOIN orders ON users.id = orders.user_id;

-- Right join
SELECT users.name, orders.order_date
FROM users
RIGHT JOIN orders ON users.id = orders.user_id;

-- Full join
SELECT users.name, orders.order_date
FROM users
FULL JOIN orders ON users.id = orders.user_id;

-- Cross join
SELECT users.name, orders.order_date
FROM users
CROSS JOIN orders;
