# Sanitizing Input in PHP

## Introduction

Sanitizing input in PHP is crucial for preventing security vulnerabilities such as SQL injection, cross-site scripting (XSS), and other attacks. Sanitizing input involves cleaning and validating user input to ensure it is safe and appropriate for use.

## Key Concepts

- **Sanitization**: Removing or escaping harmful characters from user input.
- **Validation**: Checking if the input meets certain criteria or rules.

## Sanitizing Input

PHP provides several functions for sanitizing input, including `filter_var`, `htmlspecialchars`, and `strip_tags`.

### filter_var

The `filter_var` function is used to sanitize and validate data.

### Example

```php
<?php
$email = "john.doe@example.com";
$sanitized_email = filter_var($email, FILTER_SANITIZE_EMAIL);
echo $sanitized_email; // Output: john.doe@example.com
?>
```

### htmlspecialchars

The `htmlspecialchars` function converts special characters to HTML entities, preventing XSS attacks.

### Example

```php
<?php
$input = "<script>alert('XSS');</script>";
$safe_input = htmlspecialchars($input, ENT_QUOTES, 'UTF-8');
echo $safe_input; // Output: &lt;script&gt;alert(&#039;XSS&#039;);&lt;/script&gt;
?>
```

### strip_tags

The `strip_tags` function removes HTML and PHP tags from a string.

### Example

```php
<?php
$input = "<p>Hello, <b>World</b>!</p>";
$safe_input = strip_tags($input);
echo $safe_input; // Output: Hello, World!
?>
```

## Validating Input

PHP provides several functions for validating input, including `filter_var` with validation filters.

### Example

```php
<?php
$email = "john.doe@example.com";
if (filter_var($email, FILTER_VALIDATE_EMAIL)) {
  echo "Valid email address";
} else {
  echo "Invalid email address";
}
?>
```

## Example

Combining different sanitization and validation techniques to create a secure form.

```php
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sanitizing Input Example</title>
</head>
<body>
  <h1>Contact Us</h1>
  <form action="process.php" method="post">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name"><br><br>
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email"><br><br>
    
    <label for="message">Message:</label>
    <textarea id="message" name="message" rows="4" cols="50"></textarea><br><br>
    
    <input type="submit" value="Submit">
  </form>
</body>
</html>
```

```php
<?php
// process.php
if ($_SERVER["REQUEST_METHOD"] == "POST") {
  $name = htmlspecialchars(strip_tags($_POST["name"]), ENT_QUOTES, 'UTF-8');
  $email = filter_var($_POST["email"], FILTER_SANITIZE_EMAIL);
  $message = htmlspecialchars(strip_tags($_POST["message"]), ENT_QUOTES, 'UTF-8');

  if (filter_var($email, FILTER_VALIDATE_EMAIL)) {
    echo "Name: $name<br>";
    echo "Email: $email<br>";
    echo "Message: $message<br>";
  } else {
    echo "Invalid email address";
  }
}
?>
