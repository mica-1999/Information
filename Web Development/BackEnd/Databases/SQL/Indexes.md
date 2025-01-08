# SQL Indexes

## Introduction

SQL indexes are used to improve the performance of database queries by allowing faster retrieval of records. Indexes are created on columns of a table and can significantly speed up search operations.

## Key Concepts

- **Index**: A data structure that improves the speed of data retrieval operations on a table.
- **Primary Key Index**: An index created automatically on the primary key of a table.
- **Unique Index**: An index that ensures the uniqueness of values in the indexed column.
- **Composite Index**: An index on multiple columns of a table.

## Creating Indexes

### Creating a Simple Index

You can create an index on a single column using the `CREATE INDEX` statement.

### Example

```sql
CREATE INDEX idx_name ON users(name);
```

### Creating a Unique Index

You can create a unique index to ensure that the values in the indexed column are unique.

### Example

```sql
CREATE UNIQUE INDEX idx_email ON users(email);
```

### Creating a Composite Index

You can create a composite index on multiple columns to improve the performance of queries that filter on those columns.

### Example

```sql
CREATE INDEX idx_name_age ON users(name, age);
```

## Dropping Indexes

You can drop an index using the `DROP INDEX` statement.

### Example

```sql
DROP INDEX idx_name;
```

## Example

Combining different types of indexes to improve the performance of a database.

```sql
-- Create a table
CREATE TABLE users (
  id INT PRIMARY KEY,
  name VARCHAR(100),
  email VARCHAR(100),
  age INT
);

-- Insert data into the table
INSERT INTO users (id, name, email, age) VALUES (1, 'John Doe', 'john@example.com', 30);
INSERT INTO users (id, name, email, age) VALUES (2, 'Jane Smith', 'jane@example.com', 25);

-- Create a simple index
CREATE INDEX idx_name ON users(name);

-- Create a unique index
CREATE UNIQUE INDEX idx_email ON users(email);

-- Create a composite index
CREATE INDEX idx_name_age ON users(name, age);

-- Query data using the indexes
SELECT * FROM users WHERE name = 'John Doe';
SELECT * FROM users WHERE email = 'john@example.com';
SELECT * FROM users WHERE name = 'Jane Smith' AND age = 25;

-- Drop the indexes
DROP INDEX idx_name;
DROP INDEX idx_email;
DROP INDEX idx_name_age;
