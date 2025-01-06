# CSS Selectors

## Introduction

CSS selectors are used to select the HTML elements you want to style. There are various types of selectors available in CSS.

## Basic Selectors

### Universal Selector

The universal selector (*) selects all elements.

```css
* {
  margin: 0;
  padding: 0;
}
```

### Type Selector

The type selector selects all elements of a given type.

```css
p {
  color: blue;
}
```

### Class Selector

The class selector selects all elements with a specific class attribute. It is denoted by a period (.) followed by the class name.

```css
.intro {
  font-weight: bold;
}
```

### ID Selector

The ID selector selects a single element with a specific ID attribute. It is denoted by a hash (#) followed by the ID name.

```css
#main {
  text-align: center;
}
```

## Combinator Selectors

### Descendant Selector

The descendant selector selects all elements that are descendants of a specified element.

```css
div p {
  color: green;
}
```

### Child Selector

The child selector selects all elements that are direct children of a specified element.

```css
div > p {
  color: red;
}
```

### Adjacent Sibling Selector

The adjacent sibling selector selects an element that is immediately preceded by a specified element.

```css
h1 + p {
  margin-top: 0;
}
```

### General Sibling Selector

The general sibling selector selects all elements that are preceded by a specified element.

```css
h1 ~ p {
  color: purple;
}
```

## Attribute Selectors

Attribute selectors select elements based on the presence or value of their attributes.

### Example

```css
a[target] {
  color: blue;
}

a[href="https://example.com"] {
  color: red;
}

input[type="text"] {
  border: 1px solid black;
}
```

## Pseudo-class Selectors

Pseudo-class selectors select elements based on their state.

### Example

```css
a:hover {
  color: red;
}

input:focus {
  border-color: blue;
}
```

## Pseudo-element Selectors

Pseudo-element selectors select and style parts of an element.

### Example

```css
p::first-line {
  font-weight: bold;
}

p::first-letter {
  font-size: 2em;
}
```

## Example

Combining different selectors to style a web page.

```css
/* Universal selector */
* {
  margin: 0;
  padding: 0;
}

/* Type selector */
p {
  color: blue;
}

/* Class selector */
.intro {
  font-weight: bold;
}

/* ID selector */
#main {
  text-align: center;
}

/* Descendant selector */
div p {
  color: green;
}

/* Child selector */
div > p {
  color: red;
}

/* Adjacent sibling selector */
h1 + p {
  margin-top: 0;
}

/* General sibling selector */
h1 ~ p {
  color: purple;
}

/* Attribute selector */
a[target] {
  color: blue;
}

/* Pseudo-class selector */
a:hover {
  color: red;
}

/* Pseudo-element selector */
p::first-line {
  font-weight: bold;
}
