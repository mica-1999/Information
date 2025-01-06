# Functions and Lambda Expressions in Python

## Functions

Functions in Python are blocks of reusable code that perform a specific task. They help in organizing code and avoiding repetition.

### Defining a Function

A function is defined using the `def` keyword followed by the function name and parentheses.

```python
def greet(name):
    print(f"Hello, {name}!")
```

### Calling a Function

A function is called by using its name followed by parentheses.

```python
greet("Alice")
```

### Function Parameters

Functions can accept parameters, which are specified within the parentheses.

```python
def add(a, b):
    return a + b

result = add(3, 5)
print(result)  # Output: 8
```

### Default Parameters

You can provide default values for parameters. If a value is not provided for a parameter, the default value is used.

```python
def greet(name="World"):
    print(f"Hello, {name}!")

greet()        # Output: Hello, World!
greet("Alice") # Output: Hello, Alice!
```

### Variable-Length Arguments

You can use `*args` and `**kwargs` to pass a variable number of arguments to a function.

- `*args` allows you to pass a variable number of positional arguments.
- `**kwargs` allows you to pass a variable number of keyword arguments.

```python
def print_args(*args):
    for arg in args:
        print(arg)

print_args(1, 2, 3)

def print_kwargs(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

print_kwargs(name="Alice", age=30)
```

### Return Statement

The `return` statement is used to return a value from a function.

```python
def square(x):
    return x * x

result = square(4)
print(result)  # Output: 16
```

## Lambda Expressions

Lambda expressions in Python are small anonymous functions defined using the `lambda` keyword. They are used for creating small, one-time, and inline function objects.

### Syntax

The syntax for a lambda expression is:

```python
lambda arguments: expression
```

### Example

```python
square = lambda x: x * x
print(square(5))  # Output: 25

add = lambda a, b: a + b
print(add(3, 5))  # Output: 8
```

### Using Lambda with `map()`, `filter()`, and `reduce()`

Lambda expressions are often used with functions like `map()`, `filter()`, and `reduce()`.

- `map()`: Applies a function to all items in an input list.

  ```python
  numbers = [1, 2, 3, 4, 5]
  squares = list(map(lambda x: x * x, numbers))
  print(squares)  # Output: [1, 4, 9, 16, 25]
  ```

- `filter()`: Filters items in an input list based on a condition.

  ```python
  numbers = [1, 2, 3, 4, 5]
  even_numbers = list(filter(lambda x: x % 2 == 0, numbers))
  print(even_numbers)  # Output: [2, 4]
  ```

- `reduce()`: Applies a function cumulatively to the items of an input list, from left to right, to reduce the list to a single value. (Requires `functools` module)

  ```python
  from functools import reduce

  numbers = [1, 2, 3, 4, 5]
  sum = reduce(lambda x, y: x + y, numbers)
  print(sum)  # Output: 15
  ```
