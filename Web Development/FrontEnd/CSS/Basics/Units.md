# CSS Units

## Introduction

CSS units are used to define the size of various elements in a web page. They can be broadly categorized into absolute units and relative units.

## Absolute Units

Absolute units are fixed and do not change with the context.

- **px (pixels)**: Represents a single dot on the screen.
  ```css
  width: 100px;
  ```

- **cm (centimeters)**: Represents a length in centimeters.
  ```css
  width: 10cm;
  ```

- **mm (millimeters)**: Represents a length in millimeters.
  ```css
  width: 10mm;
  ```

- **in (inches)**: Represents a length in inches.
  ```css
  width: 2in;
  ```

- **pt (points)**: Represents 1/72 of an inch.
  ```css
  font-size: 12pt;
  ```

- **pc (picas)**: Represents 1/6 of an inch.
  ```css
  font-size: 1pc;
  ```

## Relative Units

Relative units are relative to another length property. They are more flexible and scalable.

- **em**: Relative to the font-size of the element.
  ```css
  font-size: 2em; /* 2 times the current font size */
  ```

- **rem**: Relative to the font-size of the root element.
  ```css
  font-size: 1.5rem; /* 1.5 times the root element's font size */
  ```

- **% (percent)**: Relative to the parent element's size.
  ```css
  width: 50%; /* 50% of the parent element's width */
  ```

- **vw (viewport width)**: Relative to 1% of the viewport's width.
  ```css
  width: 50vw; /* 50% of the viewport's width */
  ```

- **vh (viewport height)**: Relative to 1% of the viewport's height.
  ```css
  height: 50vh; /* 50% of the viewport's height */
  ```

- **vmin**: Relative to 1% of the viewport's smaller dimension (width or height).
  ```css
  width: 50vmin; /* 50% of the smaller dimension */
  ```

- **vmax**: Relative to 1% of the viewport's larger dimension (width or height).
  ```css
  width: 50vmax; /* 50% of the larger dimension */
  ```

## Example

Combining different units to style an element.

```css
div {
  width: 50%;
  height: 100px;
  padding: 1em;
  margin: 2rem;
  font-size: 16pt;
}
