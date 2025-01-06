# CSS Animations

## Introduction

CSS animations allow you to animate the transition of CSS properties over time. They are useful for creating engaging and dynamic user interfaces.

## Key Concepts

### @keyframes

The `@keyframes` rule specifies the animation. It defines the sequence of keyframes that describe how the element should be animated.

```css
@keyframes example {
  from {background-color: red;}
  to {background-color: yellow;}
}
```

### animation-name

The `animation-name` property specifies the name of the `@keyframes` animation.

```css
div {
  animation-name: example;
}
```

### animation-duration

The `animation-duration` property specifies the duration of the animation.

```css
div {
  animation-duration: 4s;
}
```

### animation-timing-function

The `animation-timing-function` property specifies the speed curve of the animation.

```css
div {
  animation-timing-function: ease;
}
```

### animation-delay

The `animation-delay` property specifies the delay before the animation starts.

```css
div {
  animation-delay: 2s;
}
```

### animation-iteration-count

The `animation-iteration-count` property specifies the number of times the animation should be played.

```css
div {
  animation-iteration-count: infinite;
}
```

### animation-direction

The `animation-direction` property specifies whether the animation should play in reverse on alternate cycles.

```css
div {
  animation-direction: alternate;
}
```

### animation

The `animation` shorthand property sets all the animation properties in one declaration.

```css
div {
  animation: example 4s ease 2s infinite alternate;
}
```

## Example

Creating a simple animation.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>CSS Animations</title>
  <style>
    @keyframes example {
      from {background-color: red;}
      to {background-color: yellow;}
    }

    div {
      width: 100px;
      height: 100px;
      background-color: red;
      animation: example 4s ease 2s infinite alternate;
    }
  </style>
</head>
<body>
  <div></div>
</body>
</html>
```

## Animation Timing Functions

### ease

The animation starts slowly, accelerates in the middle, and slows down at the end.

```css
div {
  animation-timing-function: ease;
}
```

### linear

The animation has a constant speed from start to end.

```css
div {
  animation-timing-function: linear;
}
```

### ease-in

The animation starts slowly and accelerates towards the end.

```css
div {
  animation-timing-function: ease-in;
}
```

### ease-out

The animation starts quickly and slows down towards the end.

```css
div {
  animation-timing-function: ease-out;
}
```

### ease-in-out

The animation starts slowly, accelerates in the middle, and slows down at the end.

```css
div {
  animation-timing-function: ease-in-out;
}
```

### cubic-bezier

The `cubic-bezier` function allows you to define your own timing function.

```css
div {
  animation-timing-function: cubic-bezier(0.25, 0.1, 0.25, 1);
}
```
