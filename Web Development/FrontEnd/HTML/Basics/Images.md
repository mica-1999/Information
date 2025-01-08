# HTML Images

## Introduction

HTML images are used to embed images in a web page. They are created using the `<img>` element.

## Basic Image

A basic image is created using the `<img>` element with the `src` attribute, which specifies the path to the image file.

### Example

```html
<img src="image.jpg" alt="Description of image">
```

## Image Attributes

### Alt Attribute

The `alt` attribute provides alternative text for the image, which is displayed if the image cannot be loaded. It is also used by screen readers for accessibility.

### Example

```html
<img src="image.jpg" alt="Description of image">
```

### Width and Height Attributes

The `width` and `height` attributes specify the width and height of the image in pixels.

### Example

```html
<img src="image.jpg" alt="Description of image" width="300" height="200">
```

### Title Attribute

The `title` attribute provides additional information about the image, which is displayed as a tooltip when the mouse hovers over the image.

### Example

```html
<img src="image.jpg" alt="Description of image" title="Image Title">
```

## Responsive Images

Responsive images can be created using the `srcset` and `sizes` attributes, which allow the browser to choose the best image based on the device's screen size and resolution.

### Example

```html
<img src="image.jpg" alt="Description of image" srcset="image-300.jpg 300w, image-600.jpg 600w, image-900.jpg 900w" sizes="(max-width: 600px) 100vw, 50vw">
```

## Example

Combining different image attributes to embed an image in a web page.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HTML Images Example</title>
</head>
<body>
  <h1>HTML Images</h1>
  <img src="image.jpg" alt="Description of image" width="300" height="200" title="Image Title">
  <h2>Responsive Image</h2>
  <img src="image.jpg" alt="Description of image" srcset="image-300.jpg 300w, image-600.jpg 600w, image-900.jpg 900w" sizes="(max-width: 600px) 100vw, 50vw">
</body>
</html>
