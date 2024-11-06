Here's an example of a simple HTML page that connects to two CSS files: `reset.css` (to reset default browser styles) and `style.css` (for your custom styles). Both CSS files are located in the `css/` directory.

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sample HTML Page</title>
  <link rel="stylesheet" href="css/reset.css" /><!-- Remove default browser styles -->
  <link rel="stylesheet" href="css/style.css" /><!-- Add your own styles -->
</head>
<body>
  <header>
    <h1>Welcome to My Website</h1>
    <nav>
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">About</a></li>
        <li><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section>
      <h2>About Us</h2>
      <p>This is a sample paragraph describing the content of the page. You can customize it with your own text and styles from the CSS file.</p>
    </section>
  </main>

  <footer>
    <p>&copy; 2024 My Website. All rights reserved.</p>
  </footer>
</body>
</html>
```
### Explanation:

- **`reset.css`**: This CSS file is used to reset or normalize the browser's default styles. By resetting the styles, you can ensure a consistent appearance across different browsers.
- **`style.css`**: This file contains your custom styles that define how the elements on the page should look (colours, fonts, layout, etc.).

You would need to create the `reset.css` and `style.css` files and place them in a `css/` directory relative to the HTML file.
