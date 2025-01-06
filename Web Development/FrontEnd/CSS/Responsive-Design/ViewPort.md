# Viewport in Responsive Design

## Introduction

The viewport is the user's visible area of a web page. It varies with the device, and it will be smaller on a mobile phone than on a computer screen. Understanding and controlling the viewport is crucial for creating responsive web designs.

## Viewport Meta Tag

The viewport meta tag gives the browser instructions on how to control the page's dimensions and scaling.

### Example

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

### Attributes

- **width**: Sets the width of the viewport. You can set it to a specific number of pixels or use `device-width` to match the screen's width in device-independent pixels.
- **initial-scale**: Sets the initial zoom level when the page is first loaded.
- **maximum-scale**: Sets the maximum zoom level.
- **minimum-scale**: Sets the minimum zoom level.
- **user-scalable**: Allows or disallows the user to zoom in and out.

## Example

Combining the viewport meta tag with responsive CSS to create a mobile-friendly web page.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Design</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }
    .container {
      width: 100%;
      padding: 20px;
      box-sizing: border-box;
    }
    .box {
      background-color: lightblue;
      margin: 10px 0;
      padding: 20px;
      text-align: center;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="box">Box 1</div>
    <div class="box">Box 2</div>
    <div class="box">Box 3</div>
  </div>
</body>
</html>
