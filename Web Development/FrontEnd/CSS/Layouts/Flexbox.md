# CSS Flexbox

## Introduction

CSS Flexbox Layout is a one-dimensional layout method for arranging items in rows or columns. It is designed to provide a more efficient way to lay out, align, and distribute space among items in a container, even when their size is unknown or dynamic.

## Key Concepts

### Flex Container

A flex container is an element on which the `display: flex` property is applied. It contains flex items.

```css
.container {
  display: flex;
}
```

### Flex Items

Flex items are the direct children of the flex container.

```html
<div class="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
</div>
```

## Flex Container Properties

### flex-direction

The `flex-direction` property defines the direction in which the flex items are placed in the flex container.

```css
.container {
  display: flex;
  flex-direction: row; /* row, row-reverse, column, column-reverse */
}
```

### flex-wrap

The `flex-wrap` property specifies whether the flex items should wrap or not.

```css
.container {
  display: flex;
  flex-wrap: wrap; /* nowrap, wrap, wrap-reverse */
}
```

### justify-content

The `justify-content` property aligns the flex items along the main axis.

```css
.container {
  display: flex;
  justify-content: center; /* flex-start, flex-end, center, space-between, space-around, space-evenly */
}
```

### align-items

The `align-items` property aligns the flex items along the cross axis.

```css
.container {
  display: flex;
  align-items: center; /* flex-start, flex-end, center, baseline, stretch */
}
```

### align-content

The `align-content` property aligns the flex lines when there is extra space in the cross axis.

```css
.container {
  display: flex;
  align-content: center; /* flex-start, flex-end, center, space-between, space-around, stretch */
}
```

## Flex Item Properties

### order

The `order` property specifies the order of the flex items.

```css
.item {
  order: 2; /* default is 0 */
}
```

### flex-grow

The `flex-grow` property specifies how much a flex item will grow relative to the rest of the flex items.

```css
.item {
  flex-grow: 1; /* default is 0 */
}
```

### flex-shrink

The `flex-shrink` property specifies how much a flex item will shrink relative to the rest of the flex items.

```css
.item {
  flex-shrink: 1; /* default is 1 */
}
```

### flex-basis

The `flex-basis` property specifies the initial size of a flex item before any space distribution.

```css
.item {
  flex-basis: 100px; /* default is auto */
}
```

### align-self

The `align-self` property overrides the `align-items` property for individual flex items.

```css
.item {
  align-self: center; /* auto, flex-start, flex-end, center, baseline, stretch */
}
```

## Example

Creating a simple flexbox layout.

```html
<div class="container">
  <div class="item item1">1</div>
  <div class="item item2">2</div>
  <div class="item item3">3</div>
</div>
```

```css
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  height: 100vh;
}

.item {
  background-color: lightblue;
  padding: 20px;
  margin: 10px;
  flex-grow: 1;
  text-align: center;
}
