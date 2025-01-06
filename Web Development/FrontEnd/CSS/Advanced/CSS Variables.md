# CSS Variables

## Introduction

CSS variables, also known as custom properties, allow you to store values that you can reuse throughout your CSS. They make it easier to manage and maintain your styles.

## Defining CSS Variables

CSS variables are defined using the `--` prefix and are declared inside a CSS rule.

```css
:root {
  --main-color: blue;
  --main-padding: 10px;
}
```

## Using CSS Variables

CSS variables are accessed using the `var()` function.

```css
div {
  color: var(--main-color);
  padding: var(--main-padding);
}
```

## Example

Creating a simple example using CSS variables.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Variables</title>
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

CSS variables are inherited by default, meaning they can be used in child elements.

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

You can provide fallback values for CSS variables using the `var()` function.

```css
div {
  color: var(--main-color, red); /* If --main-color is not defined, use red */
}
```

## Example

Combining CSS variables with fallback values.

```css
:root {
  --main-color: blue;
  --secondary-color: var(--main-color, green);
}

div {
  color: var(--secondary-color);
}
```
