**CSS (Cascading Style Sheets)** is a language used to describe the presentation of a webpage written in HTML or XML. It allows you to style elements such as text, images, and layouts independently from the content itself, offering separation between content (HTML) and design (CSS). CSS enhances the appearance, layout, and interactivity of web pages.

### Key Concepts of CSS

1. **Selectors**: These define which HTML elements to style.
    - `Element selector`: targets HTML tags, like `p` (for paragraphs).
    - `Class selector`: targets elements with a specific class, like `.example`.
    - `ID selector`: targets an element with a specific ID, like `#header`.
    
2. **Properties**: These define what aspect of the element to style (e.g., color, size, spacing).
    - **color**: Changes the text color (e.g., `color: red;`).
    - **background-color**: Changes the background color of an element.
    - **width** / **height**: Defines the dimensions of an element.
3. **Values**: Specify the result of applying the property (e.g., a color, a measurement, etc.).
    
### Common CSS Commands (Properties)

1. **Text Styling**:
    - `color`: Specifies the text color.
    - `font-size`: Defines the size of the font.
    - `font-family`: Specifies the font to use (e.g., `Arial, sans-serif`).
    - `text-align`: Aligns text (`left`, `right`, `center`, `justify`).
    - `text-decoration`: Adds underlines, overlines, or strikethrough (e.g., `underline`, `none`).
    
2. **Layout**:
    - `margin`: Sets the space around an element (e.g., `margin: 10px;`).
    - `padding`: Sets the space between the element’s content and its border.
    - `border`: Adds a border around an element (e.g., `border: 1px solid black;`).
    - `display`: Controls the display type of an element (`block`, `inline`, `none`, etc.).
    - `position`: Controls the positioning of an element (`static`, `relative`, `absolute`, `fixed`, `sticky`).
    
3. **Box Model**:
    - `width` / `height`: Specifies the size of an element.
    - `padding`: Adds space between the content and the border.
    - `border`: Defines the border of the element.
    - `margin`: Adds space outside the border.
    
4. **Colors and Background**:
    - `background-color`: Sets the background color.
    - `background-image`: Specifies a background image.
    - `opacity`: Controls the transparency of an element.
    
5. **Flexbox and Grid** (for layouts):
    - `display: flex`: Enables Flexbox layout.
    - `flex-direction`: Defines the direction of flex items (e.g., `row`, `column`).
    - `display: grid`: Enables CSS Grid layout.
    - `grid-template-columns`: Defines the column structure for a grid.

### Measurement Units in CSS

1. **Absolute units**:
    - `px` (pixels): A fixed unit of length.
    - `cm`, `mm`: Centimeters and millimeters, typically used in print styles.
    - `in`: Inches, primarily for print media.

2. **Relative units**:
    - `%` (percentage): A proportion of the parent element's value.
    - `em`: Relative to the font size of the parent element.
    - `rem`: Relative to the root element’s font size.
    - `vw` (viewport width): Relative to 1% of the width of the viewport.
    - `vh` (viewport height): Relative to 1% of the height of the viewport.

### CSS Box Model

The CSS box model is a fundamental concept that affects how elements are sized and spaced on a webpage. It consists of:

1. **Content**: The actual content of the element.
2. **Padding**: Space between the content and the border.
3. **Border**: A line surrounding the padding.
4. **Margin**: Space outside the border, separating elements from one another.

### Example of CSS Code
```html
/* Styling a paragraph */
p {
  color: blue;
  font-size: 16px;
  text-align: center;
  margin: 10px;
  padding: 5px;
  border: 1px solid black;
}

/* Styling a class */
.container {
  width: 100%;
  max-width: 1200px;
  margin: 0 auto;
  display: flex;
}

/* ID selector example */
#header {
  background-color: lightgray;
  padding: 20px;
  text-align: center;
}
```

In this example:
- All paragraphs (`p`) will have blue text, centered, with margins and padding.
- `.container` is a flexible box that adapts to the width of its container.
- `#header` has a background color and padded content, styled uniquely by its ID.

CSS gives you control over how web pages look, making it a powerful tool for both web designers and developers.

## Top resources, bloggers and writers known for their expertise on CSS

1. **Chris Coyier** – _CSS-Tricks_ 
    Chris Coyier is one of the most influential voices in the CSS community. His website, [CSS-Tricks](https://css-tricks.com/), is a go-to resource for CSS tutorials, tips, and news. He covers everything from basic to advanced CSS techniques, often exploring new CSS properties and tools. His work has helped countless developers learn and improve their CSS skills.
    
2. **Jen Simmons** – _Mozilla Developer Advocate_
    Jen Simmons is a designer and developer advocate at Mozilla, specializing in layout technologies. She writes extensively about CSS, especially about new layout techniques like Grid and Flexbox. Her blog and talks at various conferences help developers grasp the latest web standards and design practices. You can find her content on [her website](https://jensimmons.com/) and on Mozilla’s MDN Web Docs.
    
3. **Rachel Andrew** – _CSS Layout News_
    Rachel Andrew is a well-known web developer, editor of [CSS Layout News](https://csslayout.news/), and co-author of the book "The CSS3 Anthology." She writes extensively about CSS, particularly about layout techniques like CSS Grid, Flexbox, and web standards. Her blog and newsletters are an excellent resource for keeping up with the latest CSS advancements.
    
4. **Lea Verou** – _CSS and Web Standards Expert_
    Lea Verou is a prominent speaker and author on web standards, CSS, and front-end development. Her blog and talks cover advanced CSS techniques, and she’s well-known for her open-source tools and libraries that help developers work with CSS. You can check out her blog at lea.verou.me.
    
5. **Ahmad Shadeed** – _CSS Architect_
    Ahmad Shadeed specializes in CSS architecture and has gained recognition for his deep dives into complex CSS concepts and layout techniques. His blog offers clear, well-explained examples on modern CSS practices. You can follow his writing on [his website](https://ishadeed.com/).
    
6. **Josh W. Comeau**
    Josh writes extensively about CSS and front-end development, with a focus on approachable explanations of complex topics. His blog, [JoshWComeau.com](https://www.joshwcomeau.com/), is popular for its hands-on tutorials and engaging writing style.

These experts regularly write in-depth articles and tutorials, making their blogs essential reading for anyone looking to deepen their understanding of CSS.

## CSS Reset

Good resources about CSS resets, here are some insightful options to explore:

1. **Josh W. Comeau's Modern CSS Reset**: This reset approach is more minimal and focuses on practical adjustments, like fixing form control inheritance and handling media elements better. It’s designed for modern web development without being overly aggressive in removing styles. You can check out his explanation and example [here](https://www.joshwcomeau.com/css/custom-css-reset/)​
    [Josh W. Comeau](https://www.joshwcomeau.com/css/custom-css-reset/)
2. **HubSpot's CSS Reset Overview**: This guide provides an introduction to what a CSS reset is, why it’s useful, and how to implement it. They also discuss the differences between a traditional CSS reset and alternatives like Normalize.css, which is less aggressive. It's a good starting point for understanding when and how to use a reset​
    [HubSpot Blog](https://blog.hubspot.com/website/css-reset)
3. **W3Things Modern CSS Reset**: This resource explains the importance of using a CSS reset to neutralize the differences across browsers. It includes examples and offers a clear path to applying resets effectively in your projects, focusing on achieving consistent styling across different browsers​
    [W3Things](https://w3things.com/blog/modern-css-reset/) 
4. **WebFX's Comparison of Reset Stylesheets**: This article reviews different reset stylesheets, such as Eric Meyer's classic reset, Normalize.css, and HTML5 Doctor's reset. It’s a good resource to understand the pros and cons of different resets and how they fit into various use cases​
    [WebFX](https://www.webfx.com/blog/web-design/css-reset-stylesheets/)
These resources should give you a well-rounded understanding of CSS resets, how they work, and the various options available for your projects.

