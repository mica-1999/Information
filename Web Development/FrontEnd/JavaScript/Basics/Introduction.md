# Introduction to JavaScript

## Introduction

JavaScript is a versatile, high-level programming language that is primarily used for creating interactive and dynamic web pages. It is an essential part of web development, alongside HTML and CSS.

## Basic Syntax

JavaScript code can be included directly in HTML using the `<script>` tag or in external files with the `.js` extension.

### Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript Example</title>
</head>
<body>
  <h1>Hello, World!</h1>
  <script>
    document.querySelector('h1').textContent = 'Hello, JavaScript!';
  </script>
</body>
</html>
```

## Variables

Variables are used to store data values. In JavaScript, you can declare variables using `var`, `let`, or `const`.

### Example

```javascript
var x = 10;
let y = 20;
const z = 30;
```

## Data Types

JavaScript supports various data types, including:

- **Number**: Represents numeric values.
  ```javascript
  let num = 42;
  ```

- **String**: Represents text.
  ```javascript
  let str = "Hello, World!";
  ```

- **Boolean**: Represents true or false values.
  ```javascript
  let isTrue = true;
  ```

- **Array**: Represents a list of values.
  ```javascript
  let arr = [1, 2, 3];
  ```

- **Object**: Represents a collection of key-value pairs.
  ```javascript
  let obj = { name: "Alice", age: 25 };
  ```

## Functions

Functions are blocks of reusable code that perform a specific task.

### Example

```javascript
function greet(name) {
  return `Hello, ${name}!`;
}

console.log(greet("Alice"));
```

## Control Flow

JavaScript provides control flow statements such as `if`, `else`, `for`, and `while` to control the execution of code.

### Example

```javascript
let x = 10;

if (x > 5) {
  console.log("x is greater than 5");
} else {
  console.log("x is not greater than 5");
}

for (let i = 0; i < 5; i++) {
  console.log(i);
}

let i = 0;
while (i < 5) {
  console.log(i);
  i++;
}
```

## Example

Combining different JavaScript concepts to create a simple program.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript Example</title>
</head>
<body>
  <h1 id="greeting">Hello, World!</h1>
  <button onclick="changeGreeting()">Change Greeting</button>

  <script>
    function changeGreeting() {
      let name = prompt("Enter your name:");
      document.getElementById("greeting").textContent = `Hello, ${name}!`;
    }
  </script>
</body>
</html>
