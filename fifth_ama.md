### 1. What is the use of create super user?
- createsuperuser is used to create an admin (superuser) account in Django.
This user can log in to the Django admin panel and has all permissions like adding, editing, and deleting any data.
```bash
python manage.py createsuperuser
```

### 2. What is serializers in django?
- Serializers in Django, mainly used in Django REST Framework (DRF), are responsible for converting complex data such as Django model instances into formats like JSON that can be sent over the internet. They also convert incoming JSON data back into Python objects. In addition to data conversion, serializers perform data validation and help in creating and updating database records through APIs.

### 3. What is self keyword in python?
- The self keyword in Python refers to the current instance of a class. It is used inside class methods to access or modify instance variables and to call other methods of the same object. Each object created from a class has its own data, and self helps Python distinguish between variables that belong to different objects.

### 4. What is urls.py file used for?
- The urls.py file is used to define URL routing in a Django project. It connects specific URL patterns to view functions or class-based views. When a user requests a URL, Django checks urls.py to determine which view should handle that request and return the appropriate response.

### 5. Why do we use views.py?
- views.py contains the main logic of a Django application. It handles incoming HTTP requests, processes data, interacts with models if required, and returns HTTP responses such as HTML pages or JSON data. Views act as a bridge between the user interface (templates) and the database (models).

### 6. What is the difference between  static and media view ?
- views.py contains the main logic of a Django application. It handles incoming HTTP requests, processes data, interacts with models if required, and returns HTTP responses such as HTML pages or JSON data. Views act as a bridge between the user interface (templates) and the database (models).

### 7. What is the use installed apps in settings.py?
- INSTALLED_APPS is a list in the settings.py file that tells Django which applications are enabled in the project. Only apps mentioned in this list can use models, run migrations, appear in the admin panel, and use templates and signals. It helps Django understand which components should be loaded and used.

### 8. What is template in django?
- A template in Django is an HTML file used to display data dynamically to the user. It uses Django Template Language (DTL) to insert variables, apply logic like loops and conditions, and render content sent from views. Templates help separate presentation logic from business logic, making the application easier to maintain.

### 9. What is models.py?
- models.py is used to define the database structure of a Django application. It contains Python classes called models, where each model represents a database table and each field represents a column in that table. Django automatically converts these models into database tables using migrations.

### 10. What is makemigrations in Django?
- makemigrations is a Django command used to create migration files based on changes made in models.py. These migration files contain instructions on how the database should be modified. This command does not apply changes to the database; it only prepares them for execution.

### 11. What is settings.py?
- makemigrations is a Django command used to create migration files based on changes made in models.py. These migration files contain instructions on how the database should be modified. This command does not apply changes to the database; it only prepares them for execution.