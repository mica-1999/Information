# Media Queries

## Introduction

Media queries are a CSS feature that allows you to apply styles based on the characteristics of the device, such as its width, height, orientation, and resolution. They are essential for creating responsive web designs that adapt to different screen sizes and devices.

## Syntax

The basic syntax of a media query is:

```css
@media (condition) {
  /* CSS rules */
}
```

### Example

```css
@media (min-width: 600px) {
  body {
    background-color: lightblue;
  }
}
```

## Common Media Query Conditions

### Width and Height

- **min-width**: Applies styles if the viewport width is greater than or equal to the specified value.
  ```css
  @media (min-width: 600px) {
    /* Styles for viewports 600px and wider */
  }
  ```

- **max-width**: Applies styles if the viewport width is less than or equal to the specified value.
  ```css
  @media (max-width: 600px) {
    /* Styles for viewports 600px and narrower */
  }
  ```

- **min-height**: Applies styles if the viewport height is greater than or equal to the specified value.
  ```css
  @media (min-height: 800px) {
    /* Styles for viewports 800px and taller */
  }
  ```

- **max-height**: Applies styles if the viewport height is less than or equal to the specified value.
  ```css
  @media (max-height: 800px) {
    /* Styles for viewports 800px and shorter */
  }
  ```

### Orientation

- **orientation: portrait**: Applies styles if the device is in portrait mode.
  ```css
  @media (orientation: portrait) {
    /* Styles for portrait orientation */
  }
  ```

- **orientation: landscape**: Applies styles if the device is in landscape mode.
  ```css
  @media (orientation: landscape) {
    /* Styles for landscape orientation */
  }
  ```

### Resolution

- **min-resolution**: Applies styles if the device resolution is greater than or equal to the specified value.
  ```css
  @media (min-resolution: 300dpi) {
    /* Styles for devices with resolution 300dpi and higher */
  }
  ```

- **max-resolution**: Applies styles if the device resolution is less than or equal to the specified value.
  ```css
  @media (max-resolution: 300dpi) {
    /* Styles for devices with resolution 300dpi and lower */
  }
  ```

## Combining Media Queries

You can combine multiple conditions using logical operators such as `and`, `or`, and `not`.

### Example

```css
@media (min-width: 600px) and (max-width: 1200px) {
  /* Styles for viewports between 600px and 1200px */
}
```

## Example

Creating a responsive design using media queries.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Design with Media Queries</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
    }

    header, main, footer {
      padding: 20px;
      text-align: center;
    }

    header {
      background-color: #333;
      color: white;
    }

    main {
      background-color: #f4f4f4;
    }

    footer {
      background-color: #333;
      color: white;
    }

    /* Tablet styles */
    @media (min-width: 600px) {
      main {
        display: flex;
        justify-content: space-around;
      }

      section {
        width: 45%;
      }
    }

    /* Desktop styles */
    @media (min-width: 1024px) {
      header, main, footer {
        max-width: 960px;
        margin: 0 auto;
      }

      main {
        justify-content: space-between;
      }

      section {
        width: 30%;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>My Website</h1>
  </header>
  <main>
    <section>
      <h2>About</h2>
      <p>This is a responsive design example using media queries.</p>
    </section>
    <section>
      <h2>Services</h2>
      <p>We offer various services.</p>
    </section>
  </main>
  <footer>
    <p>&copy; 2023 My Website</p>
  </footer>
</body>
</html>
