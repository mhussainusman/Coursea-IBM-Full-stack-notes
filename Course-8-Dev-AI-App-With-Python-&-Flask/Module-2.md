# Course 8: Developing AI Applications with Python and Flask

## Module 2: Web App Deployment using Flask

### Key Concepts
- Python libraries vs. frameworks
- Flask as a microframework for web development
- Creating and running Flask applications
- Request and Response objects in Flask
- Dynamic routes and RESTful endpoints
- HTTP status codes and error handling in Flask
- Rendering static and dynamic templates
- CRUD operations support in Flask

### Notes
Python libraries provide specific tools to simplify programming tasks, while frameworks offer predefined structures for building complete applications. Flask is a lightweight microframework with minimal dependencies, designed for building web applications. It includes features like debugging servers, routing, templates, and error handling. You can install Flask via pip and create a web app by importing and instantiating the Flask class, then running the app. Flask provides Request and Response objects for each client call, allowing access to headers, query parameters, and body data. Dynamic routes enable RESTful API endpoints. HTTP status codes indicate success, client errors, or server errors, with Flask defaulting to 200 for success but allowing explicit status setting. Flask also supports application-level error handlers and CRUD operations. Templates can be static or dynamic, rendered within Flask apps.

### Code Examples
```python
from flask import Flask, request, jsonify

app = Flask(__name__)

@app.route('/hello/<name>', methods=['GET'])
def hello(name):
    # Access query parameters
    greeting = request.args.get('greeting', 'Hello')
    return jsonify(message=f"{greeting}, {name}!"), 200

@app.errorhandler(404)
def not_found(error):
    return jsonify(error="Resource not found"), 404

if __name__ == '__main__':
    app.run(debug=True)
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| Flask() | Creates a Flask application instance |
| @app.route() | Defines a route and HTTP methods for a URL |
| request.args | Accesses query parameters from the request |
| jsonify() | Converts data to JSON response |
| app.run(debug=True) | Runs the Flask app with debug mode enabled |
| @app.errorhandler() | Defines custom error handling for HTTP errors |

### Glossary
- **Flask**: A lightweight Python web framework for building web applications.
- **Microframework**: A minimalistic framework with only essential features.
- **Request Object**: Represents the HTTP request sent by the client.
- **Response Object**: Represents the HTTP response sent back to the client.
- **Dynamic Route**: A URL route that accepts variable parameters.
- **CRUD**: Create, Read, Update, Delete operations for managing data.
- **HTTP Status Codes**: Codes indicating the result of an HTTP request (e.g., 200 for success, 404 for not found).

### Summary
This module introduced Flask as a microframework for building web applications, covering how to create and run Flask apps, handle requests and responses, use dynamic routes, and manage errors. You learned about HTTP status codes and how Flask supports CRUD operations and template rendering for both static and dynamic content.