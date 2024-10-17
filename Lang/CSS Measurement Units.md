CSS uses both absolute and relative units to define sizes, spacing, positions, and other styles. Understanding the difference between these units is essential for creating flexible and responsive web designs.

### Absolute Units

Absolute units are fixed in size and do not scale based on other elements or the browser window. They are typically based on physical measurements (like inches or centimetres) or fixed pixel values. These units are less responsive, as they don’t adapt to screen size or resolution changes.

Here are the commonly used **absolute units**:
1. **px (Pixels)**
    One pixel is a single dot on the display screen, and it’s the most commonly used unit in web design. It’s fixed, meaning 1px will always represent the same size, regardless of screen resolution or display size (though it can scale with different zoom settings in the browser).
```css
    p {
      font-size: 16px; 
    }
```

2. **in (Inches)**
    _Normally not used by Web Developers_
    One inch is exactly 96 pixels (1in = 96px) and 1in is 2.54cm. 
```css
    div {
      width: 2in; 
    }
```
    
3. **cm (Centimetres)**
    _Normally not used by Web Developers_
    One centimetre is approximately 37.8 pixels (1cm = 37.8px).
```css
     div {
       width: 5cm; 
     }
```

4. **mm (Millimetres)**
    _Normally not used by Web Developers_
    One millimetre is a tenth of a centimetre (1mm = 0.1cm = 3.78px).
```css
    div {
      height: 10mm; 
    }
```

5. **pt (Points)**
    _Normally not used by Web Developers_
    One point is 1/72 of an inch (1pt = 1/72in = 1.33px). It’s often used in typography.
```css
    h1 {
      font-size: 12pt; 
    }
```
        
6. **pc (Picas)**
    _Normally not used by Web Developers_
    One pica is equal to 12 points (1pc = 12pt = 16px). This unit is used in print media.
```css
    div {
      margin-left: 2pc; 
    }
```

### Relative Units

Relative units are defined in relation to another length property, making them more flexible and responsive. They adapt to the context, such as the parent element’s size, viewport size, or font size.

Here are the commonly used **relative units**:

1. **em**
    Relative to the font size of the parent element. If the parent element’s font size is 16px, `1em` equals 16px. `2em` would be double that size (32px).
```css
    p {
      font-size: 1.5em; /* 1.5 times the parent's font size */ 
    }
```
        
2. **rem (Root em)**
    Relative to the font size of the root element (`<html>`). This unit is more consistent than `em`, because it always references the root font size, regardless of inheritance.
```css
    html {
      font-size: 16px; 
    } 
    p {
      font-size: 2rem; /* 2 times the root font size (32px) */ 
    }
```
   
3. **% (Percentage)**
    Relative to the size of the parent element. For example, a width of `50%` means half the width of the parent element.
```css
    div {
      width: 50%; /* 50% of the parent's width */ 
    }
```
        
4. **vw (Viewport Width)**
    Relative to 1% of the width of the viewport (browser window). `100vw` is the full width of the viewport.
```css
    div {
      width: 50vw; /* 50% of the viewport width */ 
    }
```
        
5. **vh (Viewport Height)**
    Relative to 1% of the height of the viewport. `100vh` equals the full height of the viewport.
```css
    div {
      height: 100vh; /* Full viewport height */ 
    }
```
        
6. **vmin and vmax**
    `vmin` is relative to 1% of the viewport's smaller dimension (width or height), and `vmax` is relative to 1% of the viewport’s larger dimension.
```css
    div {
      width: 50vmin; /* 50% of the smaller of viewport width or height */ 
    }
```
        
7. **ch**
    Relative to the width of the "0" (zero) character in the current font. It’s often used to define width or margins based on the font.
```css
    input {
      width: 20ch; /* Width of 20 "0" characters */ 
    }
```
        
8. **ex**
    Relative to the height of the lowercase "x" in the current font. This unit is used less frequently.
```css
    p {
      line-height: 2ex; 
    }
```

### When to Use Absolute vs. Relative Units
**Absolute Units**:
    Best for print media, fixed layouts, or when you need exact sizes that won’t change regardless of the screen size.
    Defining precise print layouts or ensuring pixel-perfect elements.
- **Relative Units**:
    Ideal for responsive and flexible designs. They adapt to various screen sizes, resolutions, and user settings.
    Using `rem` or `em` for text size ensures that it scales properly if a user changes their browser’s default font size.

### Example of Absolute vs. Relative Units:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
     <meta charset="UTF-8">
     <meta name="viewport" content="width=device-width, initial-scale=1.0">
     <title>Absolute vs Relative Units</title>
     <style>
       /* Absolute units */
       .box-absolute {
         width: 200px;
         height: 100px;
         background-color: lightblue;
       }
       /* Relative units */
       .box-relative {  
         width: 50%;
         height: 50vh;
         background-color: lightgreen;
       }
     </style>
  </head> 
  <body>  
    <div class="box-absolute">
      Absolute Width and Height
    </div>
    <div class="box-relative">
      Relative Width and Height
    </div>
  </body>
</html>
```

In this example:

- The **absolute** unit box (`.box-absolute`) has a fixed width of 200px and height of 100px, which won’t change regardless of screen size.
- The **relative** unit box (`.box-relative`) adjusts its width to 50% of the parent container and its height to 50% of the viewport height, making it more flexible and responsive.

### Summary
- **Absolute units** are fixed and do not change based on other factors (good for fixed layouts or print).
- **Relative units** are more flexible and scale based on the context, making them ideal for responsive design.

Using relative units like `em`, `rem`, `vw`, and `vh` can help create a more adaptable and scalable design for different devices and screen sizes.
