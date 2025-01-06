# CSS Grid

## Introduction

CSS Grid Layout is a powerful layout system that allows you to create complex, responsive web layouts with ease. It provides a grid-based layout system, with rows and columns, making it easier to design web pages without having to use floats and positioning.

## Key Concepts

### Grid Container

A grid container is an element on which the `display: grid` property is applied. It contains grid items.

```css
.container {
  display: grid;
}
```

### Grid Items

Grid items are the direct children of the grid container.

```html
<div class="container">
  <div class="item">1</div>
  <div class="item">2</div>
  <div class="item">3</div>
</div>
```

### Grid Lines

Grid lines are the dividing lines that make up the structure of the grid. They can be horizontal or vertical.

### Grid Tracks

Grid tracks are the spaces between the grid lines. They can be rows or columns.

### Grid Cells

A grid cell is the space between two adjacent row and two adjacent column grid lines.

### Grid Areas

A grid area is a rectangular area that spans one or more grid cells.

## Defining a Grid

### Grid Template Columns and Rows

The `grid-template-columns` and `grid-template-rows` properties define the number and size of the columns and rows in the grid.

```css
.container {
  display: grid;
  grid-template-columns: 100px 200px;
  grid-template-rows: 100px 200px;
}
```

### Grid Gap

The `grid-gap` property sets the gaps (gutters) between the rows and columns.

```css
.container {
  display: grid;
  grid-template-columns: 100px 200px;
  grid-template-rows: 100px 200px;
  grid-gap: 10px;
}
```

### Placing Grid Items

Grid items can be placed in specific grid cells using the `grid-column` and `grid-row` properties.

```css
.item1 {
  grid-column: 1 / 3;
  grid-row: 1 / 2;
}
```

## Example

Creating a simple grid layout.

```html
<div class="container">
  <div class="item item1">1</div>
  <div class="item item2">2</div>
  <div class="item item3">3</div>
  <div class="item item4">4</div>
</div>
```

```css
.container {
  display: grid;
  grid-template-columns: 100px 100px;
  grid-template-rows: 100px 100px;
  grid-gap: 10px;
}

.item1 {
  grid-column: 1 / 3;
  grid-row: 1 / 2;
}

.item2 {
  grid-column: 2 / 3;
  grid-row: 2 / 3;
}

.item3 {
  grid-column: 1 / 2;
  grid-row: 2 / 3;
}

.item4 {
  grid-column: 2 / 3;
  grid-row: 1 / 2;
}
```

## Advanced Features

### Grid Template Areas

The `grid-template-areas` property allows you to define named grid areas.

```css
.container {
  display: grid;
  grid-template-areas:
    "header header"
    "sidebar main"
    "footer footer";
  grid-template-columns: 1fr 3fr;
  grid-template-rows: auto;
}

.header {
  grid-area: header;
}

.sidebar {
  grid-area: sidebar;

.main {
  grid-area: main;
}

.footer {
  grid-area: footer;
}
```

### Auto Placement

The `grid-auto-rows` and `grid-auto-columns` properties allow you to define the size of implicitly created grid tracks.

```css
.container {
  display: grid;
  grid-template-columns: 100px;
  grid-auto-rows: 50px;
}
