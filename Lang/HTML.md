HTML (Hyper Text Markup Language) is the standard language used to create and structure content on the web. It defines the structure and layout of a webpage by using a variety of elements (tags) that describe the content, such as headings, paragraphs, links, images, and more. HTML is not a programming language but a markup language, meaning it annotates text so that a browser can interpret and display it.
```html
<!DOCTYPE html>
<html>
  <head>
    <title>Page Title</title>
  </head>
  <body>
    <!-- Page content goes here -->
  </body>
</html>
```

Here’s a breakdown of some of the most important HTML tags:
### Important HTML Tags
1. **`<!DOCTYPE html>`**
    - Declares the document type and version of HTML. It tells the browser that the document is HTML5.
2. **`<html>`**
    - The root element that wraps all content in an HTML document.
3. **`<head>`**
    - Contains meta-information about the document such as the title, links to stylesheets, and metadata.
4. **`<title>`**
    - Defines the title of the document, which is displayed in the browser’s title bar or tab.
5. **`<body>`**
    - Contains the actual content of the webpage, such as text, images, links, etc.

### Content Structure Tags
6. **`<h1>` to `<h6>`**
    - Heading tags used to define different levels of headings. `<h1>` is the highest (main title), and `<h6>` is the lowest.
    - Example: `<h1>Main Title</h1>`
7. **`<p>`**
    - Represents a paragraph of text.
    - Example: `<p>This is a paragraph.</p>`
8. **`<a>`**
    - Defines a hyperlink to another document or resource.
    - Example: `<a href="https://www.example.com">Visit Example</a>`
9. **`<img>`**
    - Embeds an image into the page. It requires the `src` attribute to specify the image file and the `alt` attribute for accessibility.
    - Example: `<img src="image.jpg" alt="Description of the image">`
10. **`<ul>`, `<ol>`, and `<li>`**
    - Used to create lists. `<ul>` creates an unordered (bulleted) list, `<ol>` creates an ordered (numbered) list, and `<li>` defines each list item.
    - Example ```
        <ul>
          <li>First item</li>
          <li>Second item</li>
        </ul> ```
11. **`<div>`**
    - A container used to group other elements for styling or layout purposes. It has no specific meaning on its own.
    - Example:  ```<div>Content inside a div</div>```
12. **`<span>`**
    - Used to group inline elements. Like `<div>`, it has no inherent meaning but is useful for styling specific parts of content.
    - Example: `<span style="color: red;">Red Text</span>`
13. **`<form>`**
    - Used to create an interactive form that collects user input. Forms typically include input fields such as text boxes, checkboxes, or submit buttons.
    - Example: 
      ```
      <form action="/submit__page.php" method="post">
          <input type="text" name="name" placeholder="Your name">
          <input type="submit" value="Submit">
      </form>
      ```

### Semantic Tags
14. **`<header>`**
    - Defines the header of a document or section. It often contains logos, navigation links, or titles.
15. **`<footer>`**
    - Defines the footer of a document or section, typically containing information like copyrights or contact details.
16. **`<article>`**
    - Represents a standalone piece of content, such as a blog post or news article.
17. **`<section>`**
    - Defines a section of content that is thematically grouped.
18. **`<nav>`**
    - Represents a navigation section containing links to other parts of the website.
19. **`<aside>`**
    - Used for content that is tangentially related to the main content, often used for sidebars.
### Media Tags
20. **`<audio>` and `<video>`** 
    - Embeds audio or video files. Attributes such as `controls` are often used to provide playback controls.
    - Example: `<audio controls src="audio.mp3"></audio>`
21. **`<iframe>`**
    - Embeds another HTML document inside the current document, such as embedding a YouTube video or Google Map.
    - Example: `<iframe src="https://www.example.com"></iframe>`
### Metadata Tags
22. **`<meta>`**
    - Provides metadata such as character encoding, author, and viewport settings. It is often used for SEO and mobile optimization.
    - Example: `<meta charset="UTF-8">`

### Scripting and Linking Tags

23. **`<script>`**
        - Embeds or links JavaScript code within the HTML document.
    - Example: `<script src="app.js"></script>`
24. **`<link>`**
        - Links external resources, such as stylesheets, to the HTML document.
    - Example: `<link rel="stylesheet" href="styles.css">`
25. **`<style>`**
        - Used to define internal CSS styles directly within the HTML document.
        - Example: ```
         <style>
            body { font-family: Arial; }
         </style>
         ```
### Connecting HTML with a CSS File

By separating HTML structure from CSS styling, you can easily manage and maintain the visual design of your website without altering the HTML content.

This tells the browser to apply the styles defined in the ```style.css``` file to the HTML elements in the document. The `href` value can be a relative or absolute path to the CSS file, depending on where the file is stored. 

To connect an HTML document with a CSS file, the ```<link>``` element is used within the `<head>` section of the HTML. The ```rel="stylesheet"``` attribute specifies that the linked file is a CSS stylesheet, while the ```href="style.css"``` attribute points to the location of the CSS file. 

Here’s an example:
```html
<head>
   <link rel="stylesheet" href="style.css" /> 
</head>
```

See everything in a [HTML Example Page](Lang/html-example.md).

