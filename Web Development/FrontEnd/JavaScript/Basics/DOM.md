# JavaScript DOM Manipulation

## Introduction

The Document Object Model (DOM) is a programming interface for web documents. It represents the structure of a document as a tree of objects, allowing JavaScript to interact with and manipulate the content and structure of web pages.

## Selecting Elements

You can select elements in the DOM using methods like `getElementById`, `getElementsByClassName`, `getElementsByTagName`, `querySelector`, and `querySelectorAll`.

### Example

```javascript
let element = document.getElementById("myElement");
let elements = document.getElementsByClassName("myClass");
let tags = document.getElementsByTagName("p");
let firstElement = document.querySelector(".myClass");
let allElements = document.querySelectorAll(".myClass");
```

## Manipulating Elements

You can manipulate the content and attributes of elements using properties like `textContent`, `innerHTML`, `setAttribute`, and `style`.

### Example

```javascript
let element = document.getElementById("myElement");

// Change text content
element.textContent = "New text content";

// Change inner HTML
element.innerHTML = "<strong>Bold text</strong>";

// Set attribute
element.setAttribute("data-custom", "value");

// Change style
element.style.color = "red";
```

## Creating and Removing Elements

You can create new elements using `createElement` and append them to the DOM using `appendChild`. You can also remove elements using `removeChild`.

### Example

```javascript
let newElement = document.createElement("div");
newElement.textContent = "I am a new element";

// Append to body
document.body.appendChild(newElement);

// Remove element
document.body.removeChild(newElement);
```

## Event Handling

You can add event listeners to elements to handle user interactions like clicks, mouse movements, and key presses.

### Example

```javascript
let button = document.getElementById("myButton");

button.addEventListener("click", function() {
  alert("Button clicked!");
});
```

## Example

Combining different DOM manipulation techniques to create an interactive web page.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>DOM Manipulation Example</title>
</head>
<body>
  <h1 id="title">Hello, World!</h1>
  <button id="changeTextButton">Change Text</button>
  <button id="addElementButton">Add Element</button>
  <button id="removeElementButton">Remove Element</button>

  <script>
    let title = document.getElementById("title");
    let changeTextButton = document.getElementById("changeTextButton");
    let addElementButton = document.getElementById("addElementButton");
    let removeElementButton = document.getElementById("removeElementButton");

    changeTextButton.addEventListener("click", function() {
      title.textContent = "Hello, JavaScript!";
    });

    addElementButton.addEventListener("click", function() {
      let newElement = document.createElement("p");
      newElement.textContent = "I am a new paragraph.";
      document.body.appendChild(newElement);
    });

    removeElementButton.addEventListener("click", function() {
      let newElement = document.querySelector("p");
      if (newElement) {
        document.body.removeChild(newElement);
      }
    });
  </script>
</body>
</html>
