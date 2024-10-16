with **[HTML](Lang/HTML)**, **[CSS](Lang/CSS)**, **[JavaScript](Lang/JavaScript)**, **[Node.js](Server/App/Node.js)**, **[MongoDB](Server/DB/MongoDB)**, and **[PostgreSQL](Server/DB/PostgreSQL)** combines several technologies to create dynamic, interactive, and full-featured web applications. 
### Development Workflow
1. Frontend Development (**[HTML](Lang/HTML)**, **[CSS](Lang/CSS)**, **[JavaScript](Lang/JavaScript)**)
	* You start by designing the user interface (UI) using **[HTML](Lang/HTML)** for structure and **[CSS](Lang/CSS)** for styling.
    * **[JavaScript](Lang/JavaScript)** adds dynamic behaviour to the frontend, enabling features like live form validation, AJAX calls (to update data without reloading), and user interface interactivity.
    * The UI is created using **[HTML](Lang/HTML)**, styled with **[CSS](Lang/CSS)**, and made interactive with **[JavaScript](Lang/JavaScript)** and a framework like **[React.js](Frameworks/Frontend/React.js)** or Vue.js.
2. Backend Development (**[Node.js](Server/App/Node.js)**)
    * On the server side, **[Node.js](Server/App/Node.js)** manages the logic, handles HTTP requests, connects with the databases, and processes user data.
    * RESTful APIs can be built using **[Node.js](Server/App/Node.js)** to serve data to the frontend from the backend.
    * The server-side logic is built using **[Node.js](Server/App/Node.js)** and Express.js, handling requests, authentication, and serving data to the frontend.*
3. Database Management (**[MongoDB](Server/DB/MongoDB)**, **[PostgreSQL](Server/DB/PostgreSQL)**)
    * Data is stored and retrieved using either **[MongoDB](Server/DB/MongoDB)** (for flexible, schema-less data) or **[PostgreSQL](Server/DB/PostgreSQL)** (for relational data with defined schemas).
    * Depending on the application’s needs, either **[MongoDB](Server/DB/MongoDB)** or **[PostgreSQL](Server/DB/PostgreSQL)** is chosen for optimal data management.
4. Code Management
	Managed with **[Git](Tools/VCS/Git)**, allowing teams to collaborate and track code changes
5. Servers 
    In production, **[Nginx](Server/web/Nginx)** or **[Apache](Server/web/Apache)** serve the web app, while databases run on **[MongoDB](Server/DB/MongoDB)** Atlas or **[PostgreSQL](Server/DB/PostgreSQL)** servers.
6. Deployment: The application is deployed on platforms like Heroku or AWS, making it accessible to users globally.
This combination of technologies allows developers to build modern, scalable, and performant web applications that meet various business needs.

### Example Application: E-commerce Web App
1. Frontend:
	* Use **[HTML](Lang/HTML)** to create the structure for the product pages, user reviews, and a shopping cart.
    * Style the layout with **[CSS](Lang/CSS)** for an appealing user experience.
    * Add **[JavaScript](Lang/JavaScript)** to enable features like live product filtering, adding items to the cart without page reloads, and interactive forms for checkout.
2. Backend:
    * **[Node.js](Server/App/Node.js)** handles incoming requests like fetching product details, user authentication, and checkout processes.
    * APIs built in **[Node.js](Server/App/Node.js)** allow the frontend to request and display data, such as products, prices, and stock availability.
3. Databases:
    * Use **[MongoDB](Server/DB/MongoDB)** to store user-generated content, such as reviews, which vary in structure (title, rating, and optional comments).
    * Use **[PostgreSQL](Server/DB/PostgreSQL)** to store structured data like product information, order history, and user profiles that require relationships and complex queries.
By combining these technologies, developers can build modern, full-stack web applications that are scalable, maintainable, and performant.

# Technology Details
## 1. HTML (Hyper Text Markup Language)
**[HTML](Lang/HTML)** is the standard markup language for creating the structure of web pages. It defines elements like headings, paragraphs, links, images, forms, and other content.
Provides the foundation of the web application. It determines the page's layout, elements, and how content is structured and displayed in a browser.
## 2. CSS (Cascading Style Sheets)
**[CSS](Lang/CSS)** is used for styling and visual design, defining how **[HTML](Lang/HTML)** elements should be displayed on the screen.
Controls the presentation of the web application, including colours, fonts, spacing, layouts, and responsiveness. **[CSS](Lang/CSS)** makes the app visually appealing and ensures a consistent design across various devices.
## 3. JavaScript
**[JavaScript](Lang/JavaScript)** is a programming language that enables interactivity and dynamic behaviour on web pages.
Adds functionality to the web app, such as form validation, dynamic content updates (without reloading the page), animations, and interactions with APIs. **[JavaScript](Lang/JavaScript)** can be run both on the client side (in the browser) and on the server side (using **[Node.js](Server/App/Node.js)**).
## 4. Node.js
**[Node.js](Server/App/Node.js)** is a server-side runtime environment that allows developers to write server-side code in **[JavaScript](Lang/JavaScript)**.
**[Node.js](Server/App/Node.js)** is used to build the backend of a web application, handling requests, managing databases, and serving data to the client. It's particularly effective for building scalable, real-time web applications. The non-blocking I/O model of **[Node.js](Server/App/Node.js)** makes it efficient for handling multiple requests at once.
## 5. MongoDB
**[MongoDB](Server/DB/MongoDB)** is a NoSQL database designed to store data in a flexible, JSON-like format called BSON.
**[MongoDB](Server/DB/MongoDB)** is used in web applications to store and manage unstructured or semi-structured data. It is ideal for applications that require fast iterations and handle large amounts of data that may not fit neatly into traditional table-based structures. **[MongoDB](Server/DB/MongoDB)**’s flexibility makes it popular in applications that require scalability.
## 6. PostgreSQL
**[PostgreSQL](Server/DB/PostgreSQL)** is a powerful, open-source relational database management system (RDBMS).
Unlike **[MongoDB](Server/DB/MongoDB)**, **[PostgreSQL](Server/DB/PostgreSQL)** is used to store structured data and supports complex queries, relationships, and transactions. It’s known for its robustness, ability to handle large datasets, and compliance with SQL standards. **[PostgreSQL](Server/DB/PostgreSQL)** is preferred when data integrity and relational models are essential, such as in financial systems or applications requiring complex querying.
## 7. Tools for Development and Collaboration
### Version control with Git
**[Git](Tools/VCS/Git)** is a version control system that allows developers to track changes in their codebase, collaborate with others, and maintain different versions of their code.
It is essential for web development as it helps manage source code and collaboration in teams. With **[Git](VCS/Git)**, you can:
Track every modification to the codebase.
Work on different branches for features, bug fixes, or experiments.
Merge changes from multiple developers without losing code.
Collaborate with tools like **[GitHub](Server/VCS/GitHub)**, **[GitLab](Server/VCS/GitLab)**, or **[Bitbucket](Server/VCS/Bitbucket)** to manage repositories and review code.
### Node Package Manager (npm)
npm is a package manager for **[JavaScript](Lang/JavaScript)** and **[Node.js](Server/App/Node.js)**, which helps install and manage third-party libraries and frameworks.
npm is essential for managing dependencies and integrating external packages into your **[project](Project)**, such as libraries for frontend frameworks, backend utilities, or database connectors.
## 8. Useful Frameworks
### Layout Frameworks

#### Bootstrap

### Frontend Frameworks
#### React.js
**[React.js](Frameworks/Frontend/React.js)** is a popular frontend library for building interactive user interfaces.
It allows you to create reusable components, manage application state effectively, and optimize the performance of the UI with virtual DOM. React is widely used in modern web applications for building dynamic, responsive UIs.
#### Vue.js
**[Vue.js](Frameworks/Frontend/Vue.js)** is a progressive **[JavaScript](Lang/JavaScript)** framework for building UIs and single-page applications.
Similar to React, Vue helps developers create reusable components and handle complex user interfaces efficiently. **[Vue.js](Frameworks/Frontend/Vue.js)** is often praised for its simplicity and flexibility.
#### Angular
**[Angular](Frameworks/Frontend/Angular)** is a full-fledged frontend framework developed by Google, used to build dynamic web applications.
**[Angular](Frameworks/Frontend/Angular)** provides a complete solution for building web applications, including data binding, state management, routing, and form validation. It is particularly suitable for larger applications with complex business logic.
### Backend Frameworks
#### Express.js
**[Express.js](Frameworks/Backend/Express.js)** is a minimalist web framework for **[Node.js](Server/App/Node.js)** that simplifies the creation of server-side applications.
Express allows you to handle routes, requests, and responses easily. It’s a lightweight, unopinionated framework often used in combination with **[Node.js](Server/App/Node.js)** to create REST APIs and manage server-side logic.
#### Nest.js
**[Nest.js](Frameworks/Backend/Nest.js)** is a progressive **[Node.js](Server/App/Node.js)** framework built with TypeScript and heavily inspired by Angular.
It helps in structuring scalable server-side applications and includes many out-of-the-box features like dependency injection, modular architecture, and powerful CLI tools. It’s ideal for building large-scale, maintainable applications.
#### Koa.js
**[Koa](Frameworks/Backend/Koa.js)** is another minimal web framework, developed by the same team that created Express.
**[Koa](Frameworks/Backend/Koa.js)** is lightweight and gives developers more flexibility by removing many features that Express includes by default. It’s ideal for developers who want more control over the middleware and request/response handling.
### Databases and ORM Frameworks
#### Mongoose (for *MongoDB)
**[Mongoose](Library/DB/ORM/Mongoose)** is an Object Data Modeling (ODM) library for **[MongoDB](Server/DB/MongoDB)** and **[Node.js](Server/App/Node.js)**.
It simplifies the interaction between **[Node.js](Server/App/Node.js)** and **[MongoDB](Server/DB/MongoDB)** by providing a schema-based solution to model your application data, validating data, and managing relationships between documents.
#### Sequelize (for SQL Databases)
Sequelize is a promise-based ORM (Object-Relational Mapping) for **[Node.js](Server/App/Node.js)** that works with SQL databases like **[PostgreSQL](Server/DB/PostgreSQL)**, MySQL, SQLite, and more.
It helps developers interact with relational databases using **[JavaScript](Lang/JavaScript)** objects rather than raw SQL queries, managing data models, associations, and migrations.
#### Prisma
**[Prisma](Toolkit/DB/Prisma)** is a modern database toolkit for **[Node.js](Server/App/Node.js)** that allows you to work with SQL and NoSQL databases.
**[Prisma](Toolkit/DB/Prisma)** automates database schema migrations and makes database querying much more intuitive with a powerful type-safe API. It's commonly used with **[PostgreSQL](Server/DB/PostgreSQL)** and **[MongoDB](Server/DB/MongoDB)**.

----
## Infrastructure, Servers and Hosting
### 1. Servers
#### Application Servers
##### **[Node.js](Server/App/Node.js)** Development Server
**[Node.js](Server/App/Node.js)** can be used to run the backend server during development.
Using **[Node.js](Server/App/Node.js)** along with frameworks like **[Express.js](Frameworks/Backend/Express.js)** or Nest.js, developers can set up a local development server to handle backend logic and test APIs.
##### Webpack Dev Server
Webpack Dev Server is used to bundle and serve the frontend of a web application during development.
It provides live-reloading, hot module replacement, and automatic updates whenever code changes, making frontend development faster and more efficient.
Production Servers
#### Web Servers
##### Nginx 
**[Nginx](Server/web/Nginx)** is a high-performance web server that also functions as a reverse proxy, load balancer, and caching server.
In production, **[Nginx](Server/web/Nginx)** is used to serve static content (**[HTML](Lang/HTML)**, **[CSS](Lang/CSS)**, **[JavaScript](Lang/JavaScript)**) and forward API requests to the **[Node.js](Server/App/Node.js)** backend server. It improves security, performance, and scalability.
##### Apache
**[Apache](Server/web/Apache)** is another popular web server software that can handle HTTP requests.
Like **[Nginx](Server/web/Nginx)**, **[Apache](Server/web/Apache)** can serve static content and act as a reverse proxy for your **[Node.js](Server/App/Node.js)** applications. It’s widely used due to its flexibility and extensive documentation.
#### Database Servers
##### MongoDB
**[MongoDB](Server/DB/MongoDB)** Atlas is a cloud-based database service for **[MongoDB](Server/DB/MongoDB)**.
It allows you to run **[MongoDB](Server/DB/MongoDB)** databases on the cloud, providing scalability, security, and automated backups. This is ideal for production environments.
##### PostgreSQL
**[PostgreSQL](Server/DB/PostgreSQL)** can be hosted on cloud platforms like AWS, Google Cloud, or managed locally.
**[PostgreSQL](Server/DB/PostgreSQL)** server provides the database engine for structured, relational data. It handles data integrity, complex queries, and relationships, making it suitable for large-scale applications.
#### 2. Deployment Platforms
##### Heroku
**[Heroku](PaaS/Heroku)** is a platform-as-a-service (PaaS) that allows developers to deploy, manage, and scale applications.
It simplifies the process of deploying **[Node.js](Server/App/Node.js)**, **[MongoDB](Server/DB/MongoDB)**, and **[PostgreSQL](Server/DB/PostgreSQL)** applications. You can quickly deploy applications using **[Git](VCS/Git)** and manage everything from a cloud dashboard.
#### 3. Cloud Provider
##### DigitalOcean
**[DigitalOcean](Cloud/DigitalOcean)** provides virtual private servers (droplets) to host applications.
With **[DigitalOcean](Cloud/DigitalOcean)**, you can set up **[Node.js](Server/App/Node.js)**, **[Nginx](Server/web/Nginx)**, **[MongoDB](Server/DB/MongoDB)**, and **[PostgreSQL](Server/DB/PostgreSQL)** on a scalable, cloud-based infrastructure.
##### AWS (Amazon Web Services)
**[AWS](Cloud/AWS)** is a comprehensive cloud platform offering a range of services including virtual servers (EC2), managed databases (RDS for **[PostgreSQL](Server/DB/PostgreSQL)**), and storage solutions.
It’s a robust platform for deploying and scaling web applications. **[AWS](Cloud/AWS)** provides services like EC2 for hosting **[Node.js](Server/App/Node.js)**, S3 for serving static files, and RDS for managing databases.
#### 4. Containerization
**[Docker](Container/Docker)** is used to package applications and their dependencies into containers that can run consistently across different environments.
**[Docker](Container/Docker)** containers help developers maintain consistency between development, testing, and production environments. Tools like **[Docker](Container/Docker)** Compose allow multi-container setups, running services like the web app, database, and caching systems (e.g., **[Redis](Server/DB/Redis)**) in isolated environments.

----
