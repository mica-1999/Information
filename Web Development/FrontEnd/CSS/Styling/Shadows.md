# CSS Shadows

## Introduction

CSS shadows are used to add shadow effects to elements. There are two types of shadows in CSS: text shadows and box shadows.

## Text Shadows

The `text-shadow` property adds shadow to text.

### Syntax

```css
text-shadow: h-shadow v-shadow blur-radius color;
```

### Example

```css
p {
  text-shadow: 2px 2px 5px gray;
}
```

## Box Shadows

The `box-shadow` property adds shadow to elements.

### Syntax

```css
box-shadow: h-shadow v-shadow blur-radius spread-radius color;
```

### Example

```css
div {
  box-shadow: 5px 5px 10px 0px rgba(0, 0, 0, 0.5);
}
```

## Inset Shadows

You can create inset shadows by adding the `inset` keyword.

### Example

```css
div {
  box-shadow: inset 5px 5px 10px 0px rgba(0, 0, 0, 0.5);
}
```

## Multiple Shadows

You can add multiple shadows by separating them with commas.

### Example

```css
div {
  box-shadow: 5px 5px 10px 0px rgba(0, 0, 0, 0.5), -5px -5px 10px 0px rgba(0, 0, 0, 0.3);
}
```

## Example

Combining different shadow properties to style elements.

```css
p {
  text-shadow: 2px 2px 5px gray;
}

div {
  box-shadow: 5px 5px 10px 0px rgba(0, 0, 0, 0.5);
}

.inset {
  box-shadow: inset 5px 5px 10px 0px rgba(0, 0, 0, 0.5);
}

.multiple {
  box-shadow: 5px 5px 10px 0px rgba(0, 0, 0, 0.5), -5px -5px 10px 0px rgba(0, 0, 0, 0.3);
}
