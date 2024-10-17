CSS pseudo-classes are keywords added to selectors that specify a special state of the selected elements. They allow you to style elements based on their dynamic behaviour or their position in the document tree, without adding additional classes or IDs to the HTML.
## Commonly Used CSS Pseudo-Classes:

1. **`:link`** 
    Targets links that have not yet been visited. It typically applies to `<a>` elements with an `href` attribute.
```css
    a:link {
      color: blue;
    }
```
2. **`:visited`** 
    Applies to links that have already been visited by the user.
```css
    a:visited {
      color: lightgray;
    }
```
3. **`:hover`** 
    Applies when the user hovers their mouse pointer over an element. It's often used to create interactive effects.
```css
    a:hover {
      color: purple;
    }
```
4. **`:active`** 
    Applies while an element, like a link, is being activated (e.g., when a user clicks on it and holds down the mouse button).
```css
    a:active {
      color: red;
    }
```
5. **`:focus`** 
    Targets an element that has received focus, typically via keyboard navigation or a mouse click.
```css
    a:focus {
      outline: 2px solid blue;
    }
```
6. **`:first-child`** 
    Matches an element if it is the first child of its parent.
```css
    a:first-child {
      font-weight: bold;
    }
```
7. **`:last-child`** 
    Matches an element if it is the last child of its parent.
```css
    p:last-child {
      color: green;
    }
```
8. **`:nth-child(n)`** 
    Matches elements based on their position among siblings. You can specify `n` as a number, keyword, or formula.
```css
    li:nth-child(odd) {
      background-color: lightgray;
    }
```
9. **`:not(selector)`** 
    Selects every element that does not match the specified selector.
```css
    p:not(.highlight) {
       color: gray;
    }
```
10. **`:checked`** 
    Matches form elements like checkboxes or radio buttons that are checked.
```css
    input:checked {
      border: 2px solid green;
    }
```
11. **`:disabled`** 
    Matches form elements that are disabled and not available for interaction.
```css
    input:disabled {
      background-color: lightgray;
    }
```
12. **`:enabled`** 
    Targets form elements that are enabled.
```css
    input:enabled {
      background-color: white;
    }
```

### Special Pseudo-Classes:
- **`:first-of-type`**: Matches the first element of its type among its siblings.
- **`:last-of-type`**: Matches the last element of its type among its siblings.
- **`:nth-of-type(n)`**: Matches elements based on their position among siblings of the same type.

### Example of Combining Pseudo-Classes:
```css
a:hover, a:focus {
    color: red;
    text-decoration: underline;
}
```

### Use Cases:
- **Interactive navigation elements** (e.g., :hover, :active for buttons and links).
- **Form validation styles** (:focus, :valid, :invalid).
- **Table row highlighting** (:nth-child for alternating row colors).

Pseudo-classes are powerful in CSS for handling dynamic styles and user interactions. They let you style elements in specific states without modifying the underlying HTML structure.


# Example 
```css
a:link {
    color: #1a73e8; /* A vibrant blue for unvisited links */
    text-decoration: none;
}
a:visited {
    color: #551a8b; /* A darker, muted purple for visited links */
    text-decoration: none;
}
a:hover {
    color: #ff5722; /* A warm orange for hovered links */
    text-decoration: underline;
}
a:active {
    color: #e91e63; /* A strong pink for active links */
    text-decoration: underline;
    <!-- Click sound -->
}
```


