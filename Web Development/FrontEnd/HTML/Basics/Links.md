# HTML Links

## Introduction

HTML links are used to create hyperlinks to other web pages, resources, or locations within the same page. They are created using the `<a>` (anchor) element.

## Basic Link

A basic link is created using the `<a>` element with the `href` attribute.

### Example

```html
<a href="https://example.com">Visit Example</a>
```

## Link Attributes

### Target Attribute

The `target` attribute specifies where to open the linked document.

- `_self`: Opens the link in the same window/tab (default).
- `_blank`: Opens the link in a new window/tab.
- `_parent`: Opens the link in the parent frame.
- `_top`: Opens the link in the full body of the window.

### Example

```html
<a href="https://example.com" target="_blank">Visit Example</a>
```

### Title Attribute

The `title` attribute provides additional information about the link, which is displayed as a tooltip when the mouse hovers over the link.

### Example

```html
<a href="https://example.com" title="Go to Example">Visit Example</a>
```

## Email Links

Email links are created using the `mailto:` scheme in the `href` attribute.

### Example

```html
<a href="mailto:someone@example.com">Send Email</a>
```

## Telephone Links

Telephone links are created using the `tel:` scheme in the `href` attribute.

### Example

```html
<a href="tel:+1234567890">Call Us</a>
```

## Anchor Links

Anchor links are used to link to a specific location within the same page. They are created using the `id` attribute.

### Example

```html
<a href="#section1">Go to Section 1</a>

<h2 id="section1">Section 1</h2>
<p>This is Section 1.</p>
```

## Example

Combining different types of links in a web page.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HTML Links Example</title>
</head>
<body>
  <h1>HTML Links</h1>
  <p><a href="https://example.com" target="_blank" title="Go to Example">Visit Example</a></p>
  <p><a href="mailto:someone@example.com">Send Email</a></p>
  <p><a href="tel:+1234567890">Call Us</a></p>
  <p><a href="#section1">Go to Section 1</a></p>
  
  <h2 id="section1">Section 1</h2>
  <p>This is Section 1.</p>
</body>
</html>
