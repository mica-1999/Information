# Document Databases

## Introduction

Document databases store data in JSON-like documents. Each document contains key-value pairs and can have a nested structure. They are designed to handle semi-structured data and provide flexibility in data modeling.

## Key Concepts

- **Document**: A JSON-like structure that contains key-value pairs.
- **Collection**: A group of documents.
- **Schema-less**: Document databases do not require a fixed schema, allowing for flexible and dynamic data models.

## Example

### Document

```json
{
  "name": "John Doe",
  "age": 30,
  "address": {
    "street": "123 Main St",
    "city": "Anytown",
    "state": "CA"
  }
}
```

### Collection

```json
[
  {
    "name": "John Doe",
    "age": 30,
    "address": {
      "street": "123 Main St",
      "city": "Anytown",
      "state": "CA"
    }
  },
  {
    "name": "Jane Smith",
    "age": 25,
    "address": {
      "street": "456 Elm St",
      "city": "Othertown",
      "state": "NY"
    }
  }
]
```

## Advantages of Document Databases

- **Flexibility**: Document databases allow for flexible and dynamic data models.
- **Scalability**: Document databases can scale horizontally to handle large volumes of data.
- **Performance**: Document databases provide high performance for read and write operations.

## Disadvantages of Document Databases

- **Complexity**: Document databases can be more complex to manage and maintain compared to relational databases.
- **Consistency**: Document databases may sacrifice consistency for availability and partition tolerance (CAP theorem).
- **Limited Query Capabilities**: Document databases may have limited query capabilities compared to SQL databases.

## Example

Combining different document database concepts to create a simple application.

```json
{
  "users": [
    {
      "id": 1,
      "name": "John Doe",
      "age": 30,
      "address": {
        "street": "123 Main St",
        "city": "Anytown",
        "state": "CA"
      },
      "friends": [2]
    },
    {
      "id": 2,
      "name": "Jane Smith",
      "age": 25,
      "address": {
        "street": "456 Elm St",
        "city": "Othertown",
        "state": "NY"
      },
      "friends": [1]
    }
  ]
}
