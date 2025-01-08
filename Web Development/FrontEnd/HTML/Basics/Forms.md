# HTML Forms

## Introduction

HTML forms are used to collect user input. They contain form elements such as text fields, checkboxes, radio buttons, and submit buttons.

## Form Element

The `<form>` element is used to create an HTML form.

### Example

```html
<form action="/submit" method="post">
  <!-- Form elements go here -->
</form>
```

## Input Elements

### Text Input

The `<input>` element with `type="text"` is used to create a single-line text input field.

```html
<label for="name">Name:</label>
<input type="text" id="name" name="name">
```

### Password Input

The `<input>` element with `type="password"` is used to create a password input field.

```html
<label for="password">Password:</label>
<input type="password" id="password" name="password">
```

### Radio Buttons

The `<input>` element with `type="radio"` is used to create radio buttons.

```html
<label>
  <input type="radio" name="gender" value="male"> Male
</label>
<label>
  <input type="radio" name="gender" value="female"> Female
</label>
```

### Checkboxes

The `<input>` element with `type="checkbox"` is used to create checkboxes.

```html
<label>
  <input type="checkbox" name="subscribe" value="newsletter"> Subscribe to newsletter
</label>
```

### Submit Button

The `<input>` element with `type="submit"` is used to create a submit button.

```html
<input type="submit" value="Submit">
```

## Select Element

The `<select>` element is used to create a drop-down list.

### Example

```html
<label for="country">Country:</label>
<select id="country" name="country">
  <option value="usa">USA</option>
  <option value="canada">Canada</option>
  <option value="uk">UK</option>
</select>
```

## Textarea Element

The `<textarea>` element is used to create a multi-line text input field.

### Example

```html
<label for="message">Message:</label>
<textarea id="message" name="message" rows="4" cols="50"></textarea>
```

## Example

Combining different form elements to create a complete form.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>HTML Form Example</title>
</head>
<body>
  <h1>Contact Us</h1>
  <form action="/submit" method="post">
    <label for="name">Name:</label>
    <input type="text" id="name" name="name"><br><br>
    
    <label for="email">Email:</label>
    <input type="email" id="email" name="email"><br><br>
    
    <label for="message">Message:</label>
    <textarea id="message" name="message" rows="4" cols="50"></textarea><br><br>
    
    <label>
      <input type="checkbox" name="subscribe" value="newsletter"> Subscribe to newsletter
    </label><br><br>
    
    <input type="submit" value="Submit">
  </form>
</body>
</html>
