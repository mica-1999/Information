# SQL Transactions

## Introduction

SQL transactions are used to group multiple SQL statements into a single unit of work. Transactions ensure that a series of operations are executed in a consistent and reliable manner, providing atomicity, consistency, isolation, and durability (ACID properties).

## Key Concepts

- **Transaction**: A sequence of one or more SQL statements that are executed as a single unit of work.
- **Commit**: The operation that makes the changes made by the transaction permanent.
- **Rollback**: The operation that undoes the changes made by the transaction.

## ACID Properties

### Atomicity

Atomicity ensures that all the operations within a transaction are completed successfully. If any operation fails, the entire transaction is rolled back.

### Consistency

Consistency ensures that a transaction brings the database from one valid state to another valid state, maintaining the integrity of the data.

### Isolation

Isolation ensures that the operations within a transaction are isolated from other transactions, preventing concurrent transactions from interfering with each other.

### Durability

Durability ensures that the changes made by a committed transaction are permanent and will survive any subsequent system failures.

## Example

Combining different transaction concepts to create a reliable database operation.

```sql
-- Start a transaction
BEGIN TRANSACTION;

-- Insert data into the table
INSERT INTO users (id, name, email, age) VALUES (1, 'John Doe', 'john@example.com', 30);

-- Update data in the table
UPDATE users SET age = 31 WHERE id = 1;

-- Commit the transaction
COMMIT;

-- Rollback the transaction in case of an error
ROLLBACK;
```

## Example

Creating a transaction to transfer funds between two accounts.

```sql
-- Create a table for accounts
CREATE TABLE accounts (
  id INT PRIMARY KEY,
  name VARCHAR(100),
  balance DECIMAL(10, 2)
);

-- Insert data into the table
INSERT INTO accounts (id, name, balance) VALUES (1, 'John Doe', 1000.00);
INSERT INTO accounts (id, name, balance) VALUES (2, 'Jane Smith', 500.00);

-- Start a transaction
BEGIN TRANSACTION;

-- Transfer funds from John Doe to Jane Smith
UPDATE accounts SET balance = balance - 100.00 WHERE id = 1;
UPDATE accounts SET balance = balance + 100.00 WHERE id = 2;

-- Commit the transaction
COMMIT;

-- Rollback the transaction in case of an error
ROLLBACK;
