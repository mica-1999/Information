# CSS Syntax

## Introduction

CSS (Cascading Style Sheets) is used to style and layout web pages. The syntax of CSS consists of selectors and declaration blocks.

## Basic Syntax

A CSS rule consists of a selector and a declaration block.

```css
selector {
  property: value;
}
```

### Selector

The selector points to the HTML element you want to style.

### Declaration Block

The declaration block contains one or more declarations separated by semicolons.

### Declaration

A declaration consists of a property and a value, separated by a colon.

```css
property: value;
```

## Example

```css
p {
  color: red;
  font-size: 16px;
}
```

In this example, the selector `p` targets all `<p>` elements, and the declarations set the text color to red and the font size to 16 pixels.

## Comments

Comments in CSS are enclosed within `/*` and `*/`.

```css
/* This is a comment */
p {
  color: red; /* This is another comment */
}
```

## Grouping Selectors

You can group multiple selectors to apply the same styles to different elements.

```css
h1, h2, h3 {
  color: blue;
}
```

## Combining Selectors

You can combine selectors to apply styles based on more specific criteria.

### Descendant Selector

```css
div p {
  color: green;
}
```

### Class Selector

```css
.intro {
  font-weight: bold;
}
```

### ID Selector

```css
#main {
  text-align: center;
}
```

## Example

Combining different selectors and declarations to style a web page.

```css
/* Style for all paragraphs */
p {
  color: red;
  font-size: 16px;
}

/* Style for elements with class "intro" */
.intro {
  font-weight: bold;
}

/* Style for element with ID "main" */
#main {
  text-align: center;
}

/* Style for paragraphs inside a div */
div p {
  color: green;
}
```
