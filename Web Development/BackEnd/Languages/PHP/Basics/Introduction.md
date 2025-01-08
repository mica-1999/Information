# Introduction to PHP

## Introduction

PHP (Hypertext Preprocessor) is a popular server-side scripting language designed for web development. It is widely used to create dynamic and interactive web pages.

## Key Concepts

- **Server-Side Scripting**: PHP code is executed on the server, and the result is sent to the client's web browser.
- **Embedded in HTML**: PHP can be embedded directly within HTML code.
- **Cross-Platform**: PHP runs on various platforms, including Windows, Linux, and macOS.

## Basic Syntax

PHP code is enclosed within `<?php` and `?>` tags.

### Example

```php
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>PHP Example</title>
</head>
<body>
  <h1><?php echo "Hello, World!"; ?></h1>
</body>
</html>
```

## Variables

Variables in PHP are declared using the `$` symbol.

### Example

```php
<?php
$name = "John Doe";
$age = 30;
echo "Name: $name, Age: $age";
?>
```

## Data Types

PHP supports various data types, including:

- **String**: Represents text.
  ```php
  $str = "Hello, World!";
  ```

- **Integer**: Represents whole numbers.
  ```php
  $num = 42;
  ```

- **Float**: Represents decimal numbers.
  ```php
  $float = 3.14;
  ```

- **Boolean**: Represents true or false values.
  ```php
  $isTrue = true;
  ```

- **Array**: Represents a collection of values.
  ```php
  $arr = array(1, 2, 3);
  ```

- **Object**: Represents an instance of a class.
  ```php
  class Person {
    public $name;
    public $age;
  }
  $person = new Person();
  ```

## Control Structures

PHP provides control structures such as `if`, `else`, `for`, and `while` to control the execution of code.

### Example

```php
<?php
$x = 10;

if ($x > 5) {
  echo "x is greater than 5";
} else {
  echo "x is not greater than 5";
}

for ($i = 0; $i < 5; $i++) {
  echo $i;
}

$i = 0;
while ($i < 5) {
  echo $i;
  $i++;
}
?>
```

## Functions

Functions in PHP are blocks of reusable code that perform a specific task.

### Example

```php
<?php
function greet($name) {
  return "Hello, $name!";
}

echo greet("Alice");
?>
```

## Example

Combining different PHP concepts to create a simple program.

```php
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>PHP Example</title>
</head>
<body>
  <h1><?php echo "Hello, World!"; ?></h1>
  <p><?php
    $name = "John Doe";
    $age = 30;
    echo "Name: $name, Age: $age";
  ?></p>
  <p><?php
    function greet($name) {
      return "Hello, $name!";
    }
    echo greet("Alice");
  ?></p>
</body>
</html>
