# CSS Typography

## Introduction

Typography in CSS involves styling text to improve readability and visual appeal. It includes properties for setting font styles, sizes, weights, line heights, and more.

## Font Properties

### font-family

The `font-family` property specifies the font for an element.

```css
p {
  font-family: Arial, sans-serif;
}
```

### font-size

The `font-size` property sets the size of the font.

```css
p {
  font-size: 16px;
}
```

### font-weight

The `font-weight` property sets the weight (boldness) of the font.

```css
p {
  font-weight: bold;
}
```

### font-style

The `font-style` property sets the style of the font (normal, italic, oblique).

```css
p {
  font-style: italic;
}
```

### font-variant

The `font-variant` property sets the variant of the font (normal, small-caps).

```css
p {
  font-variant: small-caps;
}
```

### font

The `font` shorthand property sets all the font properties in one declaration.

```css
p {
  font: italic small-caps bold 16px/1.5 Arial, sans-serif;
}
```

## Text Properties

### color

The `color` property sets the color of the text.

```css
p {
  color: blue;
}
```

### text-align

The `text-align` property sets the horizontal alignment of the text.

```css
p {
  text-align: center;
}
```

### text-decoration

The `text-decoration` property sets the decoration of the text (underline, overline, line-through).

```css
p {
  text-decoration: underline;
}
```

### text-transform

The `text-transform` property controls the capitalization of the text.

```css
p {
  text-transform: uppercase;
}
```

### line-height

The `line-height` property sets the height of the lines of text.

```css
p {
  line-height: 1.5;
}
```

### letter-spacing

The `letter-spacing` property sets the space between characters.

```css
p {
  letter-spacing: 2px;
}
```

### word-spacing

The `word-spacing` property sets the space between words.

```css
p {
  word-spacing: 4px;
}
```

## Example

Combining different typography properties to style text.

```css
p {
  font-family: Arial, sans-serif;
  font-size: 16px;
  font-weight: bold;
  font-style: italic;
  color: blue;
  text-align: center;
  text-decoration: underline;
  text-transform: uppercase;
  line-height: 1.5;
  letter-spacing: 2px;
  word-spacing: 4px;
}
```
