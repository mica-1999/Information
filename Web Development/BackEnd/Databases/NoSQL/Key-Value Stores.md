# Key-Value Stores

## Introduction

Key-value stores store data as key-value pairs. Each key is unique, and the value can be any type of data. They are designed for simplicity and high performance, making them suitable for caching and session management.

## Key Concepts

- **Key**: A unique identifier for a value.
- **Value**: The data associated with a key.
- **Schema-less**: Key-value stores do not require a fixed schema, allowing for flexible and dynamic data models.

## Example

### Key-Value Pairs

```json
{
  "user:1": {
    "name": "John Doe",
    "age": 30
  },
  "user:2": {
    "name": "Jane Smith",
    "age": 25
  }
}
```

## Advantages of Key-Value Stores

- **Simplicity**: Key-value stores have a simple data model and are easy to use.
- **Performance**: Key-value stores provide high performance for read and write operations.
- **Scalability**: Key-value stores can scale horizontally to handle large volumes of data.

## Disadvantages of Key-Value Stores

- **Limited Query Capabilities**: Key-value stores may have limited query capabilities compared to SQL databases.
- **Complexity**: Key-value stores can be more complex to manage and maintain compared to relational databases.
- **Consistency**: Key-value stores may sacrifice consistency for availability and partition tolerance (CAP theorem).

## Example

Combining different key-value store concepts to create a simple application.

```json
{
  "users": {
    "user:1": {
      "name": "John Doe",
      "age": 30,
      "friends": ["user:2"]
    },
    "user:2": {
      "name": "Jane Smith",
      "age": 25,
      "friends": ["user:1"]
    }
  }
}
