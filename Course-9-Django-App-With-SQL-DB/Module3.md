# Course 9: Django Application Development with SQL and Databases

## Module 3: Full-stack Django Development

### Key Concepts
- Model-View-Controller (MVC) design pattern and Django's Model-View-Template (MVT) pattern
- Django project core files: manage.py, settings.py, urls.py
- Django admin site creation and customization
- Django Views and Templates for handling web requests and responses

### Notes
This module covers the architecture and components of Django web applications. The MVC pattern divides application logic into Model (data access), View (data presentation), and Controller (coordination). Django uses a similar MVT pattern but replaces the Controller with the Django server itself. A Django View is a Python function that processes web requests (GET, POST, etc.) and returns responses such as HTML pages, JSON, or error statuses. Templates combine static HTML with dynamic Django template tags and variables to render web pages. Core Django project files include manage.py for command-line interaction, settings.py for configuration, and urls.py for routing. The Django admin site allows superusers to manage models with customizable forms, search, and filters.

### Code Examples
```python
# Example of a simple Django View
from django.http import HttpResponse

def hello_world(request):
    return HttpResponse("Hello, world!")
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| manage.py | Command-line tool to interact with Django project |
| settings.py | Contains project settings and configurations |
| urls.py | Defines URL routing for the Django app |
| View | Python function handling web requests and returning responses |
| Template | HTML file with Django tags for dynamic content rendering |
| Admin site | Interface to manage models and data in Django |

### Glossary
- **Model**: Component that accesses and manipulates data in the application.
- **View (Django)**: Python function that processes web requests and returns responses.
- **Template**: HTML file with embedded Django code to generate dynamic web pages.
- **manage.py**: Command-line utility for Django project management.
- **Admin site**: Built-in Django interface for managing database models.

### Summary
This module explains how Django implements the MVC pattern through its MVT architecture, focusing on Views and Templates for web request handling and presentation. It also introduces core project files and the Django admin site for managing application data.