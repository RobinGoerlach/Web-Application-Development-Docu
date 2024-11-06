To organize your web development project on your disk drive, it’s essential to maintain a clear structure so that files are easy to locate and manage. Here’s a recommended folder structure for organizing HTML, CSS, JS, frameworks, and images:
### Project Root

At the top level, you should have a folder that represents the overall project. Inside this folder, structure it as follows:

#### 1. **Root Folder (e.g., `MyProject/`)**

- **index.html** (or any other main HTML file)
- **README.md** (optional, for project documentation)
- **package.json** (if using Node.js)
- **.gitignore** (if using Git for version control)
- **assets/** (optional, for storing fonts, icons, etc.)

#### 2. **Subfolders**
- **/css/** — This folder contains all your CSS files.
    
    - `styles.css` (main stylesheet)
    - `reset.css` (if you’re using a CSS reset)
    - `/frameworks/` (optional, if you are using external CSS frameworks like Bootstrap or Foundation)
- **/js/** — This folder stores JavaScript files.
    
    - `app.js` (main JavaScript file)
    - `/modules/` (if you break your JS into modules)
    - `/frameworks/` (optional, for external JS frameworks or libraries like React, Vue.js, or Angular)
- **/images/** — Store all image assets here.
    
    - Organize further by categories (e.g., `/icons/`, `/backgrounds/`, `/logos/`, etc.)
- **/fonts/** — (optional) Use this to store custom fonts or web fonts.
    
- **/build/** — (optional) If you are compiling files or minifying them (e.g., with Webpack, Gulp), store the production-ready files here. This may include compiled CSS, JS, or assets.
    
- **/vendor/** — This is where you can store external libraries and plugins (CSS frameworks, JS libraries, etc.) if they are not managed by package managers like npm or CDN links.
#### 3. Additional Tips:
- **Naming Conventions:** Use consistent naming conventions like `kebab-case` for files (`my-file.js`) and `PascalCase` for class names in your JavaScript or CSS, whichever you prefer.
- **Use Version Control:** Use Git for version control to track your changes, and have a `.gitignore` file to exclude unnecessary files or folders (like `node_modules` or `build`).
- **Frameworks/Tools:** If you’re using tools like Webpack or Parcel, you’ll need to adjust the folder structure accordingly (e.g., source files in `src/` and output files in `dist/`).
- Consider adding a Licence file.

This structure will help keep everything modular and easy to navigate for you and anyone else who works on the project.

```console
MyProject/
│   index.html
│   README.md
│   package.json
│
├───css/
│   ├── styles.css
│   └── frameworks/
│       └── bootstrap.css
│
├───js/
│   ├── app.js
│   └── frameworks/
│       └── jquery.js
│
├───images/
│   ├── icons/
│   ├── backgrounds/
│   └── logo.png
│
├───fonts/
│   └── OpenSans.ttf
│
└───build/
    ├── app.min.js
    └── styles.min.css
```