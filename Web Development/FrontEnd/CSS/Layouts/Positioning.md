# CSS Positioning

## Introduction

CSS positioning allows you to control the layout and placement of elements on a web page. There are several positioning schemes available in CSS, including static, relative, absolute, fixed, and sticky positioning.

## Positioning Schemes

### Static Positioning

Static positioning is the default positioning scheme. Elements are positioned according to the normal document flow.

```css
div {
  position: static;
}
```

### Relative Positioning

Relative positioning allows you to position an element relative to its normal position. The element remains in the document flow.

```css
div {
  position: relative;
  top: 10px;
  left: 20px;
}
```

### Absolute Positioning

Absolute positioning allows you to position an element relative to its nearest positioned ancestor (or the initial containing block if no positioned ancestor exists). The element is removed from the document flow.

```css
div {
  position: absolute;
  top: 10px;
  left: 20px;
}
```

### Fixed Positioning

Fixed positioning allows you to position an element relative to the viewport. The element is removed from the document flow and does not move when the page is scrolled.

```css
div {
  position: fixed;
  top: 10px;
  left: 20px;
}
```

### Sticky Positioning

Sticky positioning allows you to position an element based on the user's scroll position. The element toggles between relative and fixed positioning depending on the scroll position.

```css
div {
  position: sticky;
  top: 0;
}
```

## Z-Index

The `z-index` property specifies the stack order of an element. Elements with a higher `z-index` are displayed in front of elements with a lower `z-index`.

```css
div {
  position: absolute;
  z-index: 10;
}
```

## Example

Combining different positioning schemes to create a complex layout.

```css
/* Static positioning (default) */
.static {
  position: static;
}

/* Relative positioning */
.relative {
  position: relative;
  top: 10px;
  left: 20px;
}

/* Absolute positioning */
.absolute {
  position: absolute;
  top: 50px;
  left: 100px;
}

/* Fixed positioning */
.fixed {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  background-color: yellow;
}

/* Sticky positioning */
.sticky {
  position: sticky;
  top: 0;
  background-color: lightblue;
}
