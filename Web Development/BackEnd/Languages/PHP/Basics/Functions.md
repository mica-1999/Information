# PHP Functions

## Introduction

Functions in PHP are blocks of reusable code that perform a specific task. They help in organizing code and avoiding repetition.

## Defining a Function

A function is defined using the `function` keyword followed by the function name and parentheses.

### Example

```php
<?php
function greet($name) {
  return "Hello, $name!";
}
?>
```

## Calling a Function

A function is called by using its name followed by parentheses.

### Example

```php
<?php
echo greet("Alice");
?>
```

## Function Parameters

Functions can accept parameters, which are specified within the parentheses.

### Example

```php
<?php
function add($a, $b) {
  return $a + $b;
}

echo add(3, 5); // Output: 8
?>
```

## Default Parameters

You can provide default values for parameters. If a value is not provided for a parameter, the default value is used.

### Example

```php
<?php
function greet($name = "World") {
  return "Hello, $name!";
}

echo greet();        // Output: Hello, World!
echo greet("Alice"); // Output: Hello, Alice!
?>
```

## Variable-Length Arguments

You can use `...$args` to pass a variable number of arguments to a function.

### Example

```php
<?php
function sum(...$numbers) {
  $total = 0;
  foreach ($numbers as $number) {
    $total += $number;
  }
  return $total;
}

echo sum(1, 2, 3, 4); // Output: 10
?>
```

## Anonymous Functions

Anonymous functions are functions without a name. They are often used as arguments to other functions.

### Example

```php
<?php
$greet = function($name) {
  return "Hello, $name!";
};

echo $greet("Alice");
?>
```

## Example

Combining different function concepts to create a simple program.

```php
<?php
function greet($name = "World") {
  return "Hello, $name!";
}

function add($a, $b) {
  return $a + $b;
}

function sum(...$numbers) {
  $total = 0;
  foreach ($numbers as $number) {
    $total += $number;
  }
  return $total;
}

echo greet("Alice") . "<br>";
echo "3 + 5 = " . add(3, 5) . "<br>";
echo "Sum of 1, 2, 3, 4: " . sum(1, 2, 3, 4) . "<br>";

$greet = function($name) {
  return "Hello, $name!";
};

echo $greet("Bob");
?>
