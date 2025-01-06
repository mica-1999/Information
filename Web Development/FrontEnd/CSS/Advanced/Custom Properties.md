# CSS Custom Properties

## Introduction

CSS custom properties (also known as CSS variables) allow you to store values that you can reuse throughout your CSS. They make it easier to manage and maintain your styles.

## Defining Custom Properties

Custom properties are defined using the `--` prefix and are declared inside a CSS rule.

```css
:root {
  --main-color: blue;
  --main-padding: 10px;
}
```

## Using Custom Properties

Custom properties are accessed using the `var()` function.

```css
div {
  color: var(--main-color);
  padding: var(--main-padding);
}
```

## Example

Creating a simple example using custom properties.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Custom Properties</title>
  <style>
    :root {
      --main-color: blue;
      --main-padding: 10px;
      --main-margin: 20px;
    }

    div {
      color: var(--main-color);
      padding: var(--main-padding);
      margin: var(--main-margin);
      border: 1px solid var(--main-color);
    }
  </style>
</head>
<body>
  <div>Hello, World!</div>
</body>
</html>
```

## Inheritance

Custom properties are inherited by default, meaning they can be used in child elements.

```css
:root {
  --main-color: blue;
}

.parent {
  color: var(--main-color);
}

.child {
  background-color: var(--main-color);
}
```

## Fallback Values

You can provide fallback values for custom properties using the `var()` function.

```css
div {
  color: var(--main-color, red); /* If --main-color is not defined, use red */
}
```

## Example

Combining custom properties with fallback values.

```css
:root {
  --main-color: blue;
  --secondary-color: var(--main-color, green);
}

div {
  color: var(--secondary-color);
}
```
