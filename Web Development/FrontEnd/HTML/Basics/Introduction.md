# Introduction to HTML

## Introduction

HTML (HyperText Markup Language) is the standard markup language used to create web pages. It provides the structure of a web page and is used to define the content and layout.

## Basic Structure

An HTML document has a basic structure that includes the `<!DOCTYPE>`, `<html>`, `<head>`, and `<body>` elements.

### Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My First HTML Page</title>
</head>
<body>
  <h1>Hello, World!</h1>
  <p>This is my first HTML page.</p>
</body>
</html>
```

## HTML Elements

HTML elements are the building blocks of an HTML document. They are defined by tags, which are enclosed in angle brackets.

### Example

```html
<p>This is a paragraph.</p>
```

## HTML Attributes

HTML attributes provide additional information about an element. They are always included in the opening tag and usually come in name/value pairs.

### Example

```html
<a href="https://example.com">Visit Example</a>
```

## Common HTML Elements

### Headings

Headings are used to define the headings of a page. There are six levels of headings, from `<h1>` to `<h6>`.

```html
<h1>This is a heading</h1>
<h2>This is a subheading</h2>
```

### Paragraphs

Paragraphs are used to define blocks of text.

```html
<p>This is a paragraph.</p>
```

### Links

Links are used to create hyperlinks to other web pages or resources.

```html
<a href="https://example.com">Visit Example</a>
```

### Images

Images are used to embed images in a web page.

```html
<img src="image.jpg" alt="Description of image">
```

### Lists

Lists are used to group related items. There are two types of lists: ordered lists and unordered lists.

#### Ordered List

```html
<ol>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
</ol>
```

#### Unordered List

```html
<ul>
  <li>First item</li>
  <li>Second item</li>
  <li>Third item</li>
</ul>
```

## Example

Combining different HTML elements to create a simple web page.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My First HTML Page</title>
</head>
<body>
  <h1>Welcome to My Website</h1>
  <p>This is a paragraph of text on my first HTML page.</p>
  <a href="https://example.com">Visit Example</a>
  <img src="image.jpg" alt="Description of image">
  <h2>My Favorite Foods</h2>
  <ul>
    <li>Pizza</li>
    <li>Burgers</li>
    <li>Ice Cream</li>
  </ul>
</body>
</html>
