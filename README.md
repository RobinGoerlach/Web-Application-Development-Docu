# Web-Application-Development-Doku
Documentation about Web Application Development with node.js, MongoDB and PostgreSQL
Written in Obsiidian so here is a small docu about it, at the end you'll find a small 
markdown tutorial.

**Obsidian**
Obsidian is a powerful and versatile note-taking and knowledge management application, designed for individuals who want to organize information and develop a personal knowledge base. It's based on Markdown, a lightweight markup language, which allows users to create notes in plain text, making them easy to read and export.
[https://obsidian.md/download]
Key Features:
Markdown Support: Obsidian uses Markdown to format text, which makes it simple to create and edit notes with headers, lists, links, and more.
Bidirectional Links: One of Obsidian's standout features is its ability to create bidirectional links between notes. When you link one note to another, both notes recognize the connection, allowing you to build a network of interconnected information.
Graph View: This feature visually represents all the notes and their relationships in a graph, helping you to see how your knowledge is connected and navigate through your notes more intuitively.
Local Storage: Obsidian stores your notes locally on your device, giving you full control of your data. There’s no need to rely on cloud services unless you want to.
Customization: Users can customize Obsidian with community plugins, themes, and settings to create a personalized experience. These plugins can range from task management tools to code editors, significantly extending Obsidian’s functionality.
How It's Used:
Personal Knowledge Management: Many users build personal wikis by creating notes on topics and linking them together. This is useful for research, personal projects, and idea development.
Project and Task Management: Some use Obsidian to track tasks and manage projects, utilizing its linking and graph view to keep track of dependencies and progress.
Journaling: Obsidian can be used as a daily journal where each day's entries can be linked to other relevant notes (e.g., events, ideas, projects).
Learning and Study: It's popular among students and lifelong learners for organizing and reviewing study material. With features like flashcard integration and spaced repetition, it can aid in long-term learning.
Code Documentation: Developers often use Obsidian for documenting code, concepts, and projects, thanks to its compatibility with code snippets and integration with Git for version control.
Overall, Obsidian helps users create a rich, interconnected database of notes, making it a powerful tool for organizing and retrieving information in a structured, non-linear way.

**Markdown**
Markdown is a lightweight markup language used to format plain text. It’s widely used for creating formatted documents in applications like Obsidian, GitHub, and many others. Here’s a summary of the basic and commonly used Markdown syntax:

Headers
Markdown uses hash (#) symbols to define headers. The number of hashes indicates the level of the header (from 1 to 6).

# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6
Emphasis (Italic and Bold)

Italic text is enclosed in either a single asterisk (*) or an underscore (_).
*Italic* or _Italic_

Bold text is enclosed in double asterisks (**) or double underscores (__).
**Bold** or __Bold__

Bold and Italic text can be combined using triple asterisks or underscores.
***Bold and Italic*** or ___Bold and Italic___

Underline text is enclosed in <u> and </u>
<u>Underline</u>

Lists
Unordered Lists
To create unordered lists, use asterisks (*), plus signs (+), or dashes (-).

* Item 1
* Item 2
  * Subitem 1
  * Subitem 2
Ordered Lists
For ordered lists, use numbers followed by periods.

1. Item 1
2. Item 2
   1. Subitem 1
   2. Subitem 2
Links
To create a link, use square brackets [] for the link text, followed by parentheses () containing the URL.

[Obsidian](https://obsidian.md)
Images
To insert an image, use an exclamation mark ! followed by the alt text in square brackets [], and the URL or path to the image in parentheses ().

![Alt text](https://example.com/image.png)
Blockquotes
For blockquotes, use the > symbol.


> This is a blockquote.
Code
Inline code can be formatted by enclosing text with backticks `.

`inline code`
To create a code block, use triple backticks ``` and optionally specify a language for syntax highlighting.

```python
def hello_world():
    print("Hello, world!")
yaml

### **Horizontal Rules**
To create a horizontal rule, use three or more asterisks (`***`), dashes (`---`), or underscores (`___`).
```markdown
---
Tables
To create tables, use pipes (|) to define columns, and dashes (-) to define headers.

| Header 1 | Header 2 |
|----------|----------|
| Row 1    | Row 1    |
| Row 2    | Row 2    |
Strikethrough
For strikethrough text, enclose the text in double tildes (~~).

~~Strikethrough~~
Task Lists
To create a task list, use square brackets with a space [ ] for an unchecked item and [x] for a checked item.

- [ ] Task 1
- [x] Task 2
Footnotes
Markdown supports footnotes in some platforms. Define a footnote reference in the text and add the footnote itself at the bottom.

Here is a footnote reference[^1].

[^1]: This is the footnote content.
Escaping Characters
If you need to use Markdown special characters without triggering their formatting functions, precede them with a backslash \.

\*Not italicized\*
These are the basic Markdown commands that help you format your text in applications like Obsidian, GitHub, and others. Markdown's simplicity and readability make it a popular choice for documentation, notes, and web content.


Markdown Cheat Sheet: https://www.markdownguide.org/cheat-sheet/
