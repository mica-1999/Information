# CSS Borders

## Introduction

CSS borders are used to define the border area around an element. You can control the width, style, and color of the borders.

## Border Properties

### border-width

The `border-width` property sets the width of the border.

```css
div {
  border-width: 2px;
}
```

### border-style

The `border-style` property sets the style of the border.

```css
div {
  border-style: solid;
}
```

### border-color

The `border-color` property sets the color of the border.

```css
div {
  border-color: red;
}
```

### border

The `border` shorthand property sets the width, style, and color of the border in one declaration.

```css
div {
  border: 2px solid red;
}
```

## Border Sides

You can set different borders for each side of an element using the following properties:

- **border-top**
- **border-right**
- **border-bottom**
- **border-left**

### Example

```css
div {
  border-top: 2px solid red;
  border-right: 2px solid green;
  border-bottom: 2px solid blue;
  border-left: 2px solid yellow;
}
```

## Border Radius

The `border-radius` property is used to create rounded corners.

### Example

```css
div {
  border: 2px solid black;
  border-radius: 10px;
}
```

## Border Images

The `border-image` property allows you to use an image as a border.

### Example

```css
div {
  border: 10px solid transparent;
  border-image: url(border.png) 30 round;
}
```

## Example

Combining different border properties to style elements.

```css
div {
  border: 2px solid red;
  border-top: 4px dashed blue;
  border-radius: 10px;
  border-image: url(border.png) 30 round;
}
```
