### 1. What is the difference between Aggregations and Annotations?
- **Aggregation:** 
- In Django ORM, aggregation is used to perform calculations on a group of records and return a single summarized value. It combines data from multiple rows in a table to produce one result, such as the total, average, minimum, maximum, or count of a particular field.
- For example, aggregation can be used to calculate the total number of views across all videos or the average rating of all posts. Aggregation reduces the queryset to a single output and is mainly used when an overall summary of the data is required.
- **Annotation:**
- In Django ORM, annotation is used to add a calculated or derived value to each object in a queryset without reducing the number of records.
- It creates a new temporary field for every row based on a calculation, such as counting the number of comments for each video or computing a value using existing fields.

### 2. What is Models.py file in django?
- In Django, the models.py file is used to define the structure of the database for an application.
- It contains Python classes called models, where each model represents a database table and each class attribute represents a column in that table.
- Django uses these models to create, read, update, and delete data in the database through the Object Relational Mapper (ORM), without writing raw SQL queries.
- Any change made in the models.py file is reflected in the database using migrations, making it the central place for managing application data and database relationships.

### 3. What is an object in django?
- In Django, an object refers to a single instance (row) of a model stored in the database. When a model is defined in the models.py file, each time data is saved using that model, Django creates an object representing one record in the corresponding database table.
- For example, if a Video model represents a table, then each video stored in the database is an object of that model.

### 4. What is an event in DOM?
- In the DOM (Document Object Model), an event is an action or occurrence that happens in the browser and can be detected by JavaScript.
- Events are usually triggered by user interactions such as clicking a button, typing in an input field, submitting a form, moving the mouse, or loading a webpage.
- When an event occurs, the browser creates an event object and notifies the JavaScript code, allowing developers to respond by executing specific functions, such as updating the page content, validating user input, or triggering animations.

### 5. Why do we use secret key in django?
- In Django, the SECRET_KEY is a unique, random string used to provide cryptographic security to the application. 
- It is mainly used to sign session data, cookies, password reset tokens, CSRF tokens, and other security-related features so that they cannot be tampered with.
- Django relies on the secret key to ensure data integrity and protect against attacks such as cookie manipulation and request forgery.
- If the secret key is exposed or changed, previously signed data becomes invalid, which can break sessions and compromise security.

### 6. What is API?
- An API (Application Programming Interface) is a set of rules and methods that allows one software application to communicate with another.
- It acts as an intermediary that defines how requests should be made, what data can be accessed, and how responses are returned.
- APIs enable different systems to interact without needing to know each other’s internal implementation, such as a mobile app fetching data from a server or a website accessing a third-party service.
- By using APIs, developers can build modular, reusable, and scalable applications.

### 7. Django uses which database by default?
- By default, when you create a new Django project, it is configured to use SQLite, which is a lightweight, file-based database.
- SQLite is easy to set up because it does not require a separate database server and is suitable for small projects, learning, and development.
- For production applications, Django also supports other databases like PostgreSQL, MySQL, and Oracle, which can be configured in the settings.py file.

### 8. What is Django apps?
- In Django, an app is a modular component of a project that performs a specific function or feature.

### 9. What is REST API?
- A REST API (Representational State Transfer API) is a type of web API that follows a set of architectural principles for communication between client and server.
- It uses standard HTTP methods such as GET, POST, PUT, PATCH, and DELETE to perform operations on resources, which are identified using URLs.
- REST APIs are stateless, meaning each request contains all the information needed to process it, and they commonly exchange data in formats like JSON.
- REST APIs are widely used because they are simple, scalable, and easy to integrate with web and mobile applications.

### 10. What is Middleware?
- In Django, middleware is a framework of hooks that sits between the request and response processing cycle.
- It allows developers to process an incoming HTTP request before it reaches the view and modify the response before it is sent back to the client.
- Middleware is commonly used for tasks such as authentication, session management, security, logging, and request validation.
- Each middleware component performs a specific function and works together to handle cross-cutting concerns across the entire application.
