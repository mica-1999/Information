# Security Best Practices in PHP

## Introduction

Security is a critical aspect of web development. Following best practices in PHP can help protect your application from common security vulnerabilities such as SQL injection, cross-site scripting (XSS), cross-site request forgery (CSRF), and more.

## Key Concepts

- **SQL Injection**: An attack where malicious SQL code is injected into a query.
- **Cross-Site Scripting (XSS)**: An attack where malicious scripts are injected into web pages viewed by other users.
- **Cross-Site Request Forgery (CSRF)**: An attack where a user is tricked into performing actions on a web application without their consent.

## Preventing SQL Injection

Use prepared statements and parameterized queries to prevent SQL injection attacks.

### Example

```php
<?php
$dsn = 'mysql:host=localhost;dbname=testdb';
$username = 'root';
$password = '';

try {
  $pdo = new PDO($dsn, $username, $password);
  $pdo->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);

  $stmt = $pdo->prepare('SELECT * FROM users WHERE email = :email');
  $stmt->execute(['email' => $_POST['email']]);
  $user = $stmt->fetch();
  print_r($user);
} catch (PDOException $e) {
  echo "Connection failed: " . $e->getMessage();
}
?>
```

## Preventing XSS

Sanitize user input and output using functions like `htmlspecialchars` and `strip_tags`.

### Example

```php
<?php
$input = "<script>alert('XSS');</script>";
$safe_input = htmlspecialchars($input, ENT_QUOTES, 'UTF-8');
echo $safe_input; // Output: &lt;script&gt;alert(&#039;XSS&#039;);&lt;/script&gt;
?>
```

## Preventing CSRF

Use CSRF tokens to protect against CSRF attacks.

### Example

```php
<?php
session_start();

if ($_SERVER["REQUEST_METHOD"] == "POST") {
  if (!isset($_POST['csrf_token']) || $_POST['csrf_token'] !== $_SESSION['csrf_token']) {
    die("CSRF token validation failed");
  }

  // Process the form
  echo "Form submitted successfully";
}

// Generate a new CSRF token
$_SESSION['csrf_token'] = bin2hex(random_bytes(32));
?>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSRF Protection Example</title>
</head>
<body>
  <h1>Contact Us</h1>
  <form action="" method="post">
    <input type="hidden" name="csrf_token" value="<?php echo $_SESSION['csrf_token']; ?>">
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

## Password Hashing

Use password hashing functions like `password_hash` and `password_verify` to securely store and verify passwords.

### Example

```php
<?php
$password = 'secret';
$hashed_password = password_hash($password, PASSWORD_DEFAULT);

if (password_verify($password, $hashed_password)) {
  echo "Password is valid";
} else {
  echo "Invalid password";
}
?>
```

## Example

Combining different security best practices to create a secure application.

```php
<?php
session_start();

$dsn = 'mysql:host=localhost;dbname=testdb';
$username = 'root';
$password = '';

try {
  $pdo = new PDO($dsn, $username, $password);
  $pdo->setAttribute(PDO::ATTR_ERRMODE, PDO::ERRMODE_EXCEPTION);

  if ($_SERVER["REQUEST_METHOD"] == "POST") {
    if (!isset($_POST['csrf_token']) || $_POST['csrf_token'] !== $_SESSION['csrf_token']) {
      die("CSRF token validation failed");
    }

    $name = htmlspecialchars(strip_tags($_POST["name"]), ENT_QUOTES, 'UTF-8');
    $email = filter_var($_POST["email"], FILTER_SANITIZE_EMAIL);
    $message = htmlspecialchars(strip_tags($_POST["message"]), ENT_QUOTES, 'UTF-8');

    if (filter_var($email, FILTER_VALIDATE_EMAIL)) {
      $stmt = $pdo->prepare('INSERT INTO messages (name, email, message) VALUES (:name, :email, :message)');
      $stmt->execute(['name' => $name, 'email' => $email, 'message' => $message]);
      echo "Message submitted successfully";
    } else {
      echo "Invalid email address";
    }
  }

  // Generate a new CSRF token
  $_SESSION['csrf_token'] = bin2hex(random_bytes(32));
} catch (PDOException $e) {
  echo "Connection failed: " . $e->getMessage();
}
?>

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Secure Application Example</title>
</head>
<body>
  <h1>Contact Us</h1>
  <form action="" method="post">
    <input type="hidden" name="csrf_token" value="<?php echo $_SESSION['csrf_token']; ?>">
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
