# JavaScript Functions

## Introduction

Functions in JavaScript are blocks of reusable code that perform a specific task. They help in organizing code and avoiding repetition.

## Defining a Function

A function is defined using the `function` keyword followed by the function name and parentheses.

### Example

```javascript
function greet(name) {
  return `Hello, ${name}!`;
}
```

## Calling a Function

A function is called by using its name followed by parentheses.

### Example

```javascript
console.log(greet("Alice"));
```

## Function Parameters

Functions can accept parameters, which are specified within the parentheses.

### Example

```javascript
function add(a, b) {
  return a + b;
}

console.log(add(3, 5)); // Output: 8
```

## Default Parameters

You can provide default values for parameters. If a value is not provided for a parameter, the default value is used.

### Example

```javascript
function greet(name = "World") {
  return `Hello, ${name}!`;
}

console.log(greet());        // Output: Hello, World!
console.log(greet("Alice")); // Output: Hello, Alice!
```

## Arrow Functions

Arrow functions provide a shorter syntax for writing functions. They are defined using the `=>` syntax.

### Example

```javascript
const greet = (name) => `Hello, ${name}!`;

console.log(greet("Alice"));
```

## Anonymous Functions

Anonymous functions are functions without a name. They are often used as arguments to other functions.

### Example

```javascript
setTimeout(function() {
  console.log("This message is displayed after 2 seconds");
}, 2000);
```

## Immediately Invoked Function Expressions (IIFE)

An IIFE is a function that is executed immediately after it is defined.

### Example

```javascript
(function() {
  console.log("This function is executed immediately");
})();
```

## Example

Combining different function concepts to create a simple program.

```javascript
function greet(name = "World") {
  return `Hello, ${name}!`;
}

const add = (a, b) => a + b;

(function() {
  console.log(greet("Alice"));
  console.log(`3 + 5 = ${add(3, 5)}`);
})();
```
