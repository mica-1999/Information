# CSS Colors

## Introduction

CSS provides various ways to specify colors for elements. You can use color names, hexadecimal values, RGB, RGBA, HSL, and HSLA.

## Color Names

CSS supports 140 standard color names.

### Example

```css
p {
  color: red;
}
```

## Hexadecimal Values

Hexadecimal values are specified with a `#` followed by six or three hexadecimal digits.

### Example

```css
p {
  color: #ff0000; /* Red */
  background-color: #00ff00; /* Green */
}
```

## RGB Values

RGB values are specified with the `rgb()` function, which takes three values (red, green, blue) ranging from 0 to 255.

### Example

```css
p {
  color: rgb(255, 0, 0); /* Red */
  background-color: rgb(0, 255, 0); /* Green */
}
```

## RGBA Values

RGBA values are similar to RGB values but include an alpha channel for opacity. The alpha value ranges from 0 (fully transparent) to 1 (fully opaque).

### Example

```css
p {
  color: rgba(255, 0, 0, 0.5); /* Red with 50% opacity */
  background-color: rgba(0, 255, 0, 0.3); /* Green with 30% opacity */
}
```

## HSL Values

HSL values are specified with the `hsl()` function, which takes three values (hue, saturation, lightness).

### Example

```css
p {
  color: hsl(0, 100%, 50%); /* Red */
  background-color: hsl(120, 100%, 50%); /* Green */
}
```

## HSLA Values

HSLA values are similar to HSL values but include an alpha channel for opacity.

### Example

```css
p {
  color: hsla(0, 100%, 50%, 0.5); /* Red with 50% opacity */
  background-color: hsla(120, 100%, 50%, 0.3); /* Green with 30% opacity */
}
```

## Example

Combining different color properties to style elements.

```css
p {
  color: red;
  background-color: #00ff00;
}

div {
  color: rgb(255, 0, 0);
  background-color: rgba(0, 255, 0, 0.3);
}

span {
  color: hsl(0, 100%, 50%);
  background-color: hsla(120, 100%, 50%, 0.3);
}
```
