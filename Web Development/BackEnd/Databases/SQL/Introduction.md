# Introduction to SQL Databases

## Introduction

SQL (Structured Query Language) is a standard language for managing and manipulating relational databases. SQL databases are widely used for storing and retrieving structured data, and they provide powerful querying capabilities.

## Key Concepts

- **Relational Database**: A database that organizes data into tables with rows and columns.
- **Table**: A collection of related data organized into rows and columns.
- **Row**: A single record in a table.
- **Column**: A single field in a table.
- **Primary Key**: A unique identifier for each row in a table.
- **Foreign Key**: A field in one table that refers to the primary key in another table.

## SQL Statements

### Data Definition Language (DDL)

DDL statements are used to define and manage database structures.

- **CREATE**: Creates a new table or database.
  ```sql
  CREATE TABLE users (
    id INT PRIMARY KEY,
    name VARCHAR(100),
    age INT
  );
  ```

- **ALTER**: Modifies an existing table.
  ```sql
  ALTER TABLE users ADD COLUMN email VARCHAR(100);
  ```

- **DROP**: Deletes a table or database.
  ```sql
  DROP TABLE users;
  ```

### Data Manipulation Language (DML)

DML statements are used to manipulate data within tables.

- **INSERT**: Adds new rows to a table.
  ```sql
  INSERT INTO users (id, name, age) VALUES (1, 'John Doe', 30);
  ```

- **UPDATE**: Modifies existing rows in a table.
  ```sql
  UPDATE users SET age = 31 WHERE id = 1;
  ```

- **DELETE**: Removes rows from a table.
  ```sql
  DELETE FROM users WHERE id = 1;
  ```

### Data Query Language (DQL)

DQL statements are used to query data from tables.

- **SELECT**: Retrieves data from a table.
  ```sql
  SELECT * FROM users;
  ```

### Data Control Language (DCL)

DCL statements are used to control access to data.

- **GRANT**: Grants permissions to users.
  ```sql
  GRANT SELECT ON users TO 'username';
  ```

- **REVOKE**: Revokes permissions from users.
  ```sql
  REVOKE SELECT ON users FROM 'username';
  ```

## Example

Combining different SQL statements to create and manipulate a database.

```sql
-- Create a new table
CREATE TABLE users (
  id INT PRIMARY KEY,
  name VARCHAR(100),
  age INT
);

-- Insert data into the table
INSERT INTO users (id, name, age) VALUES (1, 'John Doe', 30);
INSERT INTO users (id, name, age) VALUES (2, 'Jane Smith', 25);

-- Query data from the table
SELECT * FROM users;

-- Update data in the table
UPDATE users SET age = 31 WHERE id = 1;

-- Delete data from the table
DELETE FROM users WHERE id = 1;

-- Drop the table
DROP TABLE users;
