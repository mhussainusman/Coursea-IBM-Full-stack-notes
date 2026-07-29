# Course 6: Developing Back-End Apps with Node.js and Express
## Module 3: Express Web Application Framework

### Key Concepts
- Use of third-party packages and npm to extend and manage Node.js applications.
- MVC architecture divides back-end applications into model, view, and controller.
- REST API frameworks communicate using HTTP methods.
- Express framework abstracts low-level details and supports routing and middleware.
- Middleware types include application-level, router-level, error handling, built-in, and third-party.
- Template rendering enables dynamic content generation on the server.
- jsonwebtoken package is used for user authentication in Express apps.

### Notes
This module covers essential back-end development concepts using Node.js and Express. Developers extend Node.js functionality with third-party packages managed via npm. The MVC architecture organizes code into three parts to separate concerns. REST APIs use HTTP methods for communication, and Express simplifies server-side programming by abstracting complex details. Routing can be managed globally or per router, and middleware plays a key role in processing requests and responses. Template rendering allows servers to dynamically generate HTML content. For security, the jsonwebtoken package is integrated to authenticate users effectively.

### Code Examples
```javascript
// Requiring jsonwebtoken package for authentication
const jwt = require('jsonwebtoken');

// Example middleware function to verify token
function authenticateToken(req, res, next) {
  const token = req.headers['authorization'];
  if (!token) return res.sendStatus(401);
  jwt.verify(token, process.env.ACCESS_TOKEN_SECRET, (err, user) => {
    if (err) return res.sendStatus(403);
    req.user = user;
    next();
  });
}
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| npm | Manages Node.js packages |
| MVC | Architectural pattern: Model, View, Controller |
| Express | Web framework for Node.js |
| Middleware | Functions that process requests/responses |
| jsonwebtoken | Package for user authentication |
| Template rendering | Server-side dynamic content generation |

### Glossary
- **npm**: Node Package Manager, used to install and manage Node.js packages.
- **MVC (Model-View-Controller)**: Design pattern dividing application logic, UI, and input control.
- **REST API**: Web API that uses HTTP methods for communication.
- **Middleware**: Software that intercepts and processes requests/responses in Express.
- **jsonwebtoken**: Library to create and verify JSON Web Tokens for authentication.
- **Template rendering**: Process of generating HTML dynamically on the server.

### Summary
This module equips you with foundational knowledge to build back-end applications using Node.js and Express. It emphasizes managing packages with npm, structuring applications with MVC, handling routing and middleware, and implementing authentication with JSON Web Tokens. These concepts are critical for developing scalable and secure server-side applications.