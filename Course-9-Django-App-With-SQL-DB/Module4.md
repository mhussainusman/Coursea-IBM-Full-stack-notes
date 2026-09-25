# Course 9: Django Application Development with SQL and Databases

## Module 4: Module Completion Summary

### Key Concepts
- Function-based and class-based views in Django, including generic views for common tasks.
- Authentication and authorization using Django's User model and extending it for custom user types.
- Integration of Bootstrap for front-end styling in Django templates.
- Management of static files in Django projects with namespacing and static file finders.
- Deployment of Django apps using WSGI/ASGI interfaces to communicate with web servers.
- Use of cloud services (IaaS and PaaS) to simplify app deployment and infrastructure management.

### Notes
This module consolidates essential Django development skills, focusing on views, authentication, front-end integration, static file management, and deployment. It explains that both function-based and class-based views are Python functions, with class-based views subclassing Django's View class and using methods like get and post to handle HTTP requests. Django's built-in generic views help speed up development by providing reusable components. Authentication validates user identity, while authorization controls access permissions, managed through Django's User model and related groups and permissions. Bootstrap is introduced as a front-end framework to enhance UI design, which can be linked directly in templates or included as static files. Static files are organized with app-specific subfolders to avoid naming conflicts, and Django provides tools to locate and collect these files for deployment. Finally, deploying Django apps requires interfaces like WSGI or ASGI to connect with web servers, and cloud platforms offer infrastructure and platform services to ease deployment and scalability.

### Code Examples
```python
from django.views import View
from django.http import HttpResponse

class MyView(View):
    def get(self, request):
        return HttpResponse('Hello, this is a GET request')

    def post(self, request):
        return HttpResponse('Hello, this is a POST request')
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| Function-based view | A Python function handling HTTP requests |
| Class-based view | A class subclassing Django's View to handle requests |
| Generic views | Pre-built class-based views for common tasks |
| User model | Django's model for authentication and authorization |
| Bootstrap | Front-end framework for styling web pages |
| STATICFILES_FINDERS | Django components to locate static files |
| WSGI/ASGI | Interfaces for Django apps to communicate with web servers |

### Glossary
- **Function-based view**: A view implemented as a Python function to handle HTTP requests.
- **Class-based view**: A view implemented as a Python class, subclassing Django's View, with methods like get and post.
- **Generic views**: Predefined class-based views provided by Django to simplify common web development tasks.
- **Authentication**: The process of verifying a user's identity.
- **Authorization**: The process of checking user permissions to access resources.
- **Bootstrap**: A free front-end framework providing HTML and CSS templates for web development.
- **Static files**: Files like CSS, JavaScript, and images served by Django for the front-end.
- **WSGI (Web Server Gateway Interface)**: A Python standard interface between web servers and web applications.
- **ASGI (Asynchronous Server Gateway Interface)**: An interface supporting asynchronous communication between web servers and applications.

### Summary
This module equips learners with foundational Django skills, covering views, user authentication and authorization, front-end integration with Bootstrap, static file management, and deployment strategies. It emphasizes practical approaches to building scalable and maintainable Django applications ready for production environments.