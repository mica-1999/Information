# SQL Normalization

## Introduction

Normalization is the process of organizing data in a database to reduce redundancy and improve data integrity. It involves dividing a database into tables and defining relationships between them according to certain rules, known as normal forms.

## Normal Forms

### First Normal Form (1NF)

A table is in 1NF if:
- All columns contain atomic (indivisible) values.
- Each column contains values of a single type.
- Each column has a unique name.
- The order in which data is stored does not matter.

### Example

```sql
CREATE TABLE users (
  id INT PRIMARY KEY,
  name VARCHAR(100),
  age INT
);
```

### Second Normal Form (2NF)

A table is in 2NF if:
- It is in 1NF.
- All non-key columns are fully dependent on the primary key.

### Example

```sql
CREATE TABLE orders (
  order_id INT PRIMARY KEY,
  user_id INT,
  order_date DATE,
  FOREIGN KEY (user_id) REFERENCES users(id)
);
```

### Third Normal Form (3NF)

A table is in 3NF if:
- It is in 2NF.
- All non-key columns are non-transitively dependent on the primary key (i.e., no transitive dependencies).

### Example

```sql
CREATE TABLE products (
  product_id INT PRIMARY KEY,
  product_name VARCHAR(100),
  price DECIMAL(10, 2)
);

CREATE TABLE order_items (
  order_item_id INT PRIMARY KEY,
  order_id INT,
  product_id INT,
  quantity INT,
  FOREIGN KEY (order_id) REFERENCES orders(order_id),
  FOREIGN KEY (product_id) REFERENCES products(product_id)
);
```

## Advantages of Normalization

- **Reduces Redundancy**: Normalization eliminates duplicate data, reducing storage requirements.
- **Improves Data Integrity**: Normalization ensures that data is consistent and accurate.
- **Simplifies Maintenance**: Normalization makes it easier to update and maintain the database.

## Disadvantages of Normalization

- **Complexity**: Normalization can make the database schema more complex.
- **Performance**: Normalization can lead to more complex queries and slower performance due to the need for joins.

## Example

Combining different normalization concepts to create a normalized database schema.

```sql
-- Create a table for users
CREATE TABLE users (
  id INT PRIMARY KEY,
  name VARCHAR(100),
  age INT
);

-- Create a table for orders
CREATE TABLE orders (
  order_id INT PRIMARY KEY,
  user_id INT,
  order_date DATE,
  FOREIGN KEY (user_id) REFERENCES users(id)
);

-- Create a table for products
CREATE TABLE products (
  product_id INT PRIMARY KEY,
  product_name VARCHAR(100),
  price DECIMAL(10, 2)
);

-- Create a table for order items
CREATE TABLE order_items (
  order_item_id INT PRIMARY KEY,
  order_id INT,
  product_id INT,
  quantity INT,
  FOREIGN KEY (order_id) REFERENCES orders(order_id),
  FOREIGN KEY (product_id) REFERENCES products(product_id)
);
