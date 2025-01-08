# Graph Databases

## Introduction

Graph databases store data as nodes and edges, representing entities and their relationships. They are designed for applications that require complex relationships and queries, such as social networks, recommendation systems, and fraud detection.

## Key Concepts

- **Node**: An entity in the graph.
- **Edge**: A relationship between two nodes.
- **Property**: A key-value pair associated with a node or edge.

## Example

### Graph

```json
{
  "nodes": [
    { "id": 1, "name": "John Doe" },
    { "id": 2, "name": "Jane Smith" }
  ],
  "edges": [
    { "from": 1, "to": 2, "relationship": "friend" }
  ]
}
```

## Advantages of Graph Databases

- **Complex Relationships**: Graph databases can efficiently handle complex relationships and queries.
- **Flexibility**: Graph databases allow for flexible and dynamic data models.
- **Performance**: Graph databases provide high performance for read and write operations.

## Disadvantages of Graph Databases

- **Complexity**: Graph databases can be more complex to manage and maintain compared to relational databases.
- **Scalability**: Graph databases may have limited scalability compared to other NoSQL databases.
- **Limited Query Capabilities**: Graph databases may have limited query capabilities compared to SQL databases.

## Example

Combining different graph database concepts to create a simple application.

```json
{
  "users": [
    {
      "id": 1,
      "name": "John Doe",
      "age": 30,
      "friends": [2]
    },
    {
      "id": 2,
      "name": "Jane Smith",
      "age": 25,
      "friends": [1]
    }
  ],
  "relationships": [
    {
      "from": 1,
      "to": 2,
      "type": "friend"
    }
  ]
}
