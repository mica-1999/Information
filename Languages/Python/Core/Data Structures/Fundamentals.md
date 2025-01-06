# Fundamentals of Data Structures in Python

## Table of Contents
1. Introduction
2. Lists
3. Tuples
4. Sets
5. Dictionaries
6. Conclusion

## Introduction
Data structures are a fundamental aspect of programming in Python. They allow you to store and organize data efficiently. This document covers the basic data structures in Python, including lists, tuples, sets, and dictionaries.

## Lists
Lists are ordered, mutable collections of items. They are defined using square brackets `[]`.

```python
# Example of a list
fruits = ["apple", "banana", "cherry"]
```

### Common List Operations
- **Accessing Elements**: `fruits[0]` returns `"apple"`
- **Appending Elements**: `fruits.append("date")`
- **Removing Elements**: `fruits.remove("banana")`

## Tuples
Tuples are ordered, immutable collections of items. They are defined using parentheses `()`.

```python
# Example of a tuple
coordinates = (10, 20)
```

### Common Tuple Operations
- **Accessing Elements**: `coordinates[0]` returns `10`
- **Unpacking**: `x, y = coordinates`

## Sets
Sets are unordered collections of unique items. They are defined using curly braces `{}`.

```python
# Example of a set
unique_numbers = {1, 2, 3, 4}
```

### Common Set Operations
- **Adding Elements**: `unique_numbers.add(5)`
- **Removing Elements**: `unique_numbers.remove(3)`
- **Set Operations**: Union, Intersection, Difference

## Dictionaries
Dictionaries are unordered collections of key-value pairs. They are defined using curly braces `{}` with a colon `:` separating keys and values.

```python
# Example of a dictionary
person = {"name": "Alice", "age": 30}
```

### Common Dictionary Operations
- **Accessing Values**: `person["name"]` returns `"Alice"`
- **Adding Key-Value Pairs**: `person["city"] = "New York"`
- **Removing Key-Value Pairs**: `del person["age"]`

## Conclusion
Understanding these fundamental data structures is crucial for effective programming in Python. They provide the foundation for more complex data manipulation and algorithms.
