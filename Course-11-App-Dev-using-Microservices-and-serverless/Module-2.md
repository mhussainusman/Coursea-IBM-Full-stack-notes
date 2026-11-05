# Course 11: Application Development using Microservices and Serverless

## Module 2: Web API Essentials: REST API and GraphQL (Module Completion Summary)

### Key Concepts
- REST APIs provide flexible, uniform, stateless, and scalable interfaces between components using HTTP methods like POST, GET, PUT, and DELETE.
- API Gateway acts as a unified entry point to backend services, enabling scalability and integration of additional services.
- Tools such as Flask, cURL, Postman, Swagger, and OpenAPI specification support creating, testing, documenting, and interacting with REST APIs.

### Notes
This module covers the fundamentals of REST APIs, emphasizing their stateless and scalable nature, and how they use standard HTTP methods for communication. REST is an architectural style that defines how applications interact over the web. API Gateway serves as a critical component that provides a single access point to backend services, facilitating easier scaling and service replacement. The module also introduces practical tools: Flask for hosting Python web applications, cURL and Postman for making API requests, and Swagger along with OpenAPI for documenting and testing APIs effectively.

### Code Examples
```python
from flask import Flask, jsonify, request

app = Flask(__name__)

@app.route('/hello', methods=['GET'])
def hello_world():
    return jsonify(message="Hello, World!")

if __name__ == '__main__':
    app.run(debug=True)
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| REST API | Provides a stateless, scalable interface using HTTP methods |
| API Gateway | Unified access point to backend services, enabling scalability |
| Flask | Micro web framework for Python applications |
| cURL | Command-line tool to transfer data with URLs |
| Postman | Tool for building, testing, and using APIs |
| Swagger | Tool for documenting and testing APIs |
| OpenAPI Specification | Standard format for representing APIs |

### Glossary
- **REST API**: An architectural style for designing networked applications using stateless communication and standard HTTP methods.
- **API Gateway**: A server that acts as an API front-end, handling requests, routing them to appropriate services, and managing security and scaling.
- **Flask**: A lightweight Python web framework used to build web applications and APIs.
- **cURL**: A command-line tool to send requests and transfer data over various protocols including HTTP.
- **Postman**: A graphical tool to create, test, and manage APIs.
- **Swagger**: A framework for API documentation and testing.
- **OpenAPI Specification**: A standard way to describe RESTful APIs for documentation and automation.

### Summary
This module provides a comprehensive overview of REST APIs, their design principles, and the tools used to create, test, and document them. Understanding API Gateway's role and using frameworks like Flask alongside tools such as cURL, Postman, and Swagger equips learners to build scalable and maintainable web services.