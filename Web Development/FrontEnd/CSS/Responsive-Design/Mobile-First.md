# Mobile-First Design

## Introduction

Mobile-first design is a design strategy that prioritizes the mobile user experience. It involves designing for smaller screens first and then progressively enhancing the design for larger screens. This approach ensures that the core content and functionality are accessible on all devices.

## Key Concepts

- **Progressive Enhancement**: Start with a basic design that works on all devices and add enhancements for larger screens.
- **Content Prioritization**: Focus on delivering the most important content and functionality to mobile users.

## Example

Creating a mobile-first design using CSS.

### HTML

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Mobile-First Design</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>My Website</h1>
  </header>
  <main>
    <section>
      <h2>About</h2>
      <p>This is a mobile-first design example.</p>
    </section>
    <section>
      <h2>Services</h2>
      <p>We offer various services.</p>
    </section>
  </main>
  <footer>
    <p>&copy; 2023 My Website</p>
  </footer>
</body>
</html>
```

### CSS

```css
/* Mobile styles */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

header, main, footer {
  padding: 20px;
  text-align: center;
}

header {
  background-color: #333;
  color: white;
}

main {
  background-color: #f4f4f4;
}

footer {
  background-color: #333;
  color: white;
}

/* Tablet styles */
@media (min-width: 600px) {
  main {
    display: flex;
    justify-content: space-around;
  }

  section {
    width: 45%;
  }
}

/* Desktop styles */
@media (min-width: 1024px) {
  header, main, footer {
    max-width: 960px;
    margin: 0 auto;
  }

  main {
    justify-content: space-between;
  }

  section {
    width: 30%;
  }
}
