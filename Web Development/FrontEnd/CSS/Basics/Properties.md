# CSS Properties

## Introduction

CSS properties are used to style and layout HTML elements. There are numerous properties available in CSS, each serving a specific purpose.

## Common CSS Properties

### Color and Background

- **color**: Sets the text color.
  ```css
  color: red;
  ```

- **background-color**: Sets the background color of an element.
  ```css
  background-color: yellow;
  ```

- **background-image**: Sets a background image for an element.
  ```css
  background-image: url('image.jpg');
  ```

### Text

- **font-size**: Sets the size of the font.
  ```css
  font-size: 16px;
  ```

- **font-family**: Sets the font family.
  ```css
  font-family: Arial, sans-serif;
  ```

- **font-weight**: Sets the weight (boldness) of the font.
  ```css
  font-weight: bold;
  ```

- **text-align**: Sets the horizontal alignment of text.
  ```css
  text-align: center;
  ```

- **text-decoration**: Sets the decoration of text (underline, overline, line-through).
  ```css
  text-decoration: underline;
  ```

### Box Model

- **width**: Sets the width of an element.
  ```css
  width: 100px;
  ```

- **height**: Sets the height of an element.
  ```css
  height: 100px;
  ```

- **margin**: Sets the margin area on all four sides of an element.
  ```css
  margin: 10px;
  ```

- **padding**: Sets the padding area on all four sides of an element.
  ```css
  padding: 10px;
  ```

- **border**: Sets the border around an element.
  ```css
  border: 1px solid black;
  ```

### Display and Positioning

- **display**: Sets the display behavior of an element.
  ```css
  display: block;
  ```

- **position**: Sets the positioning method of an element.
  ```css
  position: absolute;
  ```

- **top, right, bottom, left**: Sets the position of an absolutely positioned element.
  ```css
  top: 10px;
  left: 20px;
  ```

- **z-index**: Sets the stack order of an element.
  ```css
  z-index: 1;
  ```

### Flexbox

- **display: flex**: Enables flexbox layout.
  ```css
  display: flex;
  ```

- **flex-direction**: Sets the direction of the flex items.
  ```css
  flex-direction: row;
  ```

- **justify-content**: Aligns the flex items along the main axis.
  ```css
  justify-content: center;
  ```

- **align-items**: Aligns the flex items along the cross axis.
  ```css
  align-items: center;
  ```

## Example

Combining different properties to style an element.

```css
div {
  width: 200px;
  height: 100px;
  margin: 20px;
  padding: 10px;
  border: 2px solid black;
  background-color: lightblue;
  color: darkblue;
  font-size: 18px;
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
}
