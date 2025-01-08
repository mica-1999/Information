# JavaScript Events

## Introduction

JavaScript events are actions or occurrences that happen in the browser, such as clicks, key presses, or mouse movements. You can use event listeners to execute code in response to these events.

## Adding Event Listeners

You can add event listeners to elements using the `addEventListener` method.

### Example

```javascript
let button = document.getElementById("myButton");

button.addEventListener("click", function() {
  alert("Button clicked!");
});
```

## Common Events

### Click Event

The `click` event is triggered when an element is clicked.

### Example

```javascript
let button = document.getElementById("myButton");

button.addEventListener("click", function() {
  alert("Button clicked!");
});
```

### Mouse Events

Mouse events include `mouseover`, `mouseout`, `mousedown`, `mouseup`, and `mousemove`.

### Example

```javascript
let element = document.getElementById("myElement");

element.addEventListener("mouseover", function() {
  element.style.backgroundColor = "yellow";
});

element.addEventListener("mouseout", function() {
  element.style.backgroundColor = "";
});
```

### Keyboard Events

Keyboard events include `keydown`, `keyup`, and `keypress`.

### Example

```javascript
document.addEventListener("keydown", function(event) {
  console.log(`Key pressed: ${event.key}`);
});
```

### Form Events

Form events include `submit`, `change`, `focus`, and `blur`.

### Example

```javascript
let form = document.getElementById("myForm");

form.addEventListener("submit", function(event) {
  event.preventDefault();
  alert("Form submitted!");
});
```

## Event Object

The event object contains information about the event, such as the target element, the type of event, and any additional data.

### Example

```javascript
let button = document.getElementById("myButton");

button.addEventListener("click", function(event) {
  console.log(`Event type: ${event.type}`);
  console.log(`Target element: ${event.target}`);
});
```

## Example

Combining different event listeners to create an interactive web page.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>JavaScript Events Example</title>
</head>
<body>
  <h1 id="title">Hello, World!</h1>
  <button id="changeTextButton">Change Text</button>
  <input type="text" id="textInput" placeholder="Type something...">
  <form id="myForm">
    <input type="text" name="name" placeholder="Name">
    <button type="submit">Submit</button>
  </form>

  <script>
    let title = document.getElementById("title");
    let changeTextButton = document.getElementById("changeTextButton");
    let textInput = document.getElementById("textInput");
    let form = document.getElementById("myForm");

    changeTextButton.addEventListener("click", function() {
      title.textContent = "Hello, JavaScript!";
    });

    textInput.addEventListener("input", function(event) {
      console.log(`Input value: ${event.target.value}`);
    });

    form.addEventListener("submit", function(event) {
      event.preventDefault();
      alert("Form submitted!");
    });
  </script>
</body>
</html>
