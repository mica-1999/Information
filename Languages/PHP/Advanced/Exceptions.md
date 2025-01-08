# PHP Exception Handling

## Introduction

Exception handling in PHP allows you to handle errors gracefully and maintain the normal flow of the program. It uses the `try`, `catch`, and `finally` blocks to catch and handle exceptions.

## Key Concepts

- **Exception**: An error that occurs during the execution of a program.
- **try Block**: Contains the code that might raise an exception.
- **catch Block**: Contains the code that handles the exception.
- **finally Block**: Contains the code that runs regardless of whether an exception is raised or not.

## Basic try-catch

The `try` block contains the code that might raise an exception, and the `catch` block contains the code that handles the exception.

### Example

```php
<?php
try {
  $x = 1 / 0;
} catch (DivisionByZeroError $e) {
  echo "Cannot divide by zero";
}
?>
```

## Multiple catch Blocks

You can have multiple `catch` blocks to handle different types of exceptions.

### Example

```php
<?php
try {
  $x = intdiv(1, 0);
} catch (DivisionByZeroError $e) {
  echo "Division by zero error";
} catch (Exception $e) {
  echo "General exception";
}
?>
```

## finally Block

The `finally` block runs regardless of whether an exception is raised or not. It is typically used for cleanup actions.

### Example

```php
<?php
try {
  $x = 1 / 0;
} catch (DivisionByZeroError $e) {
  echo "Cannot divide by zero";
} finally {
  echo "This will always run";
}
?>
```

## Throwing Exceptions

You can throw exceptions using the `throw` keyword.

### Example

```php
<?php
function checkPositive($number) {
  if ($number < 0) {
    throw new Exception("Number must be positive");
  }
  return $number;
}

try {
  checkPositive(-1);
} catch (Exception $e) {
  echo $e->getMessage();
}
?>
```

## Custom Exceptions

You can define custom exceptions by creating a new class that inherits from the built-in `Exception` class.

### Example

```php
<?php
class CustomError extends Exception {}

try {
  throw new CustomError("This is a custom error");
} catch (CustomError $e) {
  echo $e->getMessage();
}
?>
```

## Example

Combining different exception handling constructs to create a robust program.

```php
<?php
function divide($a, $b) {
  try {
    if ($b == 0) {
      throw new DivisionByZeroError("Cannot divide by zero");
    }
    return
