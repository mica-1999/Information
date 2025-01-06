# CSS Transitions

## Introduction

CSS transitions allow you to change property values smoothly (over a given duration) instead of instantly. They are useful for creating animations and enhancing user experience.

## Key Concepts

### transition-property

The `transition-property` property specifies the name of the CSS property to which the transition is applied.

```css
div {
  transition-property: width;
}
```

### transition-duration

The `transition-duration` property specifies the duration of the transition.

```css
div {
  transition-duration: 2s;
}
```

### transition-timing-function

The `transition-timing-function` property specifies the speed curve of the transition.

```css
div {
  transition-timing-function: ease;
}
```

### transition-delay

The `transition-delay` property specifies the delay before the transition starts.

```css
div {
  transition-delay: 1s;
}
```

### transition

The `transition` shorthand property sets all the transition properties in one declaration.

```css
div {
  transition: width 2s ease 1s;
}
```

## Example

Creating a simple transition effect.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Transitions</title>
  <style>
    div {
      width: 100px;
      height: 100px;
      background-color: lightblue;
      transition: width 2s, height 2s, background-color 2s, transform 2s;
    }

    div:hover {
      width: 200px;
      height: 200px;
      background-color: lightgreen;
      transform: rotate(45deg);
    }
  </style>
</head>
<body>
  <div></div>
</body>
</html>
```

## Transition Timing Functions

### ease

The transition starts slowly, accelerates in the middle, and slows down at the end.

```css
div {
  transition-timing-function: ease;
}
```

### linear

The transition has a constant speed from start to end.

```css
div {
  transition-timing-function: linear;
}
```

### ease-in

The transition starts slowly and accelerates towards the end.

```css
div {
  transition-timing-function: ease-in;
}
```

### ease-out

The transition starts quickly and slows down towards the end.

```css
div {
  transition-timing-function: ease-out;
}
```

### ease-in-out

The transition starts slowly, accelerates in the middle, and slows down at the end.

```css
div {
  transition-timing-function: ease-in-out;
}
```

### cubic-bezier

The `cubic-bezier` function allows you to define your own timing function.

```css
div {
  transition-timing-function: cubic-bezier(0.25, 0.1, 0.25, 1);
}
```
