# Python Variables and Data Types

## Variables

Variables in Python are used to store data values. A variable is created the moment you first assign a value to it.

### Variable Assignment

```python
x = 5
y = "Hello, World!"
```

### Variable Naming Rules

- Variable names must start with a letter or the underscore character.
- Variable names cannot start with a number.
- Variable names can only contain alpha-numeric characters and underscores (A-z, 0-9, and _).
- Variable names are case-sensitive (age, Age, and AGE are three different variables).

## Data Types

Python has several built-in data types that are used to store different types of data.

### Numeric Types

- **int**: Integer numbers
  ```python
  x = 10
  ```
- **float**: Floating-point numbers
  ```python
  y = 10.5
  ```
- **complex**: Complex numbers
  ```python
  z = 1 + 2j
  ```

### Text Type

- **str**: String
  ```python
  s = "Hello, World!"
  ```

### Sequence Types

- **list**: Ordered, mutable collection of items
  ```python
  my_list = [1, 2, 3, "apple", "banana"]
  ```
- **tuple**: Ordered, immutable collection of items
  ```python
  my_tuple = (1, 2, 3, "apple", "banana")
  ```
- **range**: Sequence of numbers
  ```python
  my_range = range(6)
  ```

### Mapping Type

- **dict**: Unordered, mutable collection of key-value pairs
  ```python
  my_dict = {"name": "John", "age": 30}
  ```

### Set Types

- **set**: Unordered collection of unique items
  ```python
  my_set = {1, 2, 3, "apple", "banana"}
  ```
- **frozenset**: Immutable version of a set
  ```python
  my_frozenset = frozenset({1, 2, 3, "apple", "banana"})
  ```

### Boolean Type

- **bool**: Represents True or False
  ```python
  is_true = True
  is_false = False
  ```

### Binary Types

- **bytes**: Immutable sequence of bytes
  ```python
  my_bytes = b"Hello"
  ```
- **bytearray**: Mutable sequence of bytes
  ```python
  my_bytearray = bytearray(5)
  ```
- **memoryview**: Memory view object
  ```python
  my_memoryview = memoryview(bytes(5))
  ```

## Type Conversion

You can convert from one type to another using the built-in functions.

### Example

```python
x = 5          # int
y = float(x)   # convert from int to float
z = str(x)     # convert from int to string
```

## Checking Data Type

You can check the data type of a variable using the `type()` function.

### Example

```python
x = 5
print(type(x))  # Output: <class 'int'>
