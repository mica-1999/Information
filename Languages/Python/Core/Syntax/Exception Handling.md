# Exception Handling in Python

## Introduction

Exception handling in Python allows you to handle errors gracefully and maintain the normal flow of the program. It uses the `try`, `except`, `else`, and `finally` blocks to catch and handle exceptions.

## Key Concepts

- **Exception**: An error that occurs during the execution of a program.
- **try Block**: Contains the code that might raise an exception.
- **except Block**: Contains the code that handles the exception.
- **else Block**: Contains the code that runs if no exceptions are raised.
- **finally Block**: Contains the code that runs regardless of whether an exception is raised or not.

## How Exception Handling Works

### Basic try-except

The `try` block contains the code that might raise an exception, and the `except` block contains the code that handles the exception.

```python
try:
    x = 1 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
```

### Multiple except Blocks

You can have multiple `except` blocks to handle different types of exceptions.

```python
try:
    x = int("abc")
except ValueError:
    print("ValueError: Invalid literal for int()")
except ZeroDivisionError:
    print("ZeroDivisionError: Cannot divide by zero")
```

### else Block

The `else` block runs if no exceptions are raised in the `try` block.

```python
try:
    x = 1 / 1
except ZeroDivisionError:
    print("Cannot divide by zero")
else:
    print("No exceptions raised")
```

### finally Block

The `finally` block runs regardless of whether an exception is raised or not. It is typically used for cleanup actions.

```python
try:
    x = 1 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
finally:
    print("This will always run")
```

## Raising Exceptions

You can raise exceptions using the `raise` keyword.

```python
def check_positive(number):
    if number < 0:
        raise ValueError("Number must be positive")
    return number

try:
    check_positive(-1)
except ValueError as e:
    print(e)
```

## Custom Exceptions

You can define custom exceptions by creating a new class that inherits from the built-in `Exception` class.

```python
class CustomError(Exception):
    pass

try:
    raise CustomError("This is a custom error")
except CustomError as e:
    print(e)
```

## Example

Combining different exception handling constructs to create a robust program.

```python
def divide(a, b):
    try:
        result = a / b
    except ZeroDivisionError:
        print("Cannot divide by zero")
    except TypeError:
        print("Both arguments must be numbers")
    else:
        print(f"Result: {result}")
    finally:
        print("Execution completed")

divide(10, 2)
divide(10, 0)
divide(10, "a")
