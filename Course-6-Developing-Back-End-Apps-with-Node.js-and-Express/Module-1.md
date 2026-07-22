# Course 6: Developing Back-End Apps with Node.js and Express
## Module 1: Introduction to Server-Side JavaScript

### Key Concepts
- Backend technologies and their components
- Differences between require and import statements in Node.js
- Types of Node.js modules and package installation scopes

### Notes
Backend technologies encompass servers, programming languages, frameworks, and hardware that support server-side operations. Node.js serves as the server-side runtime for JavaScript, enabling JavaScript to run outside the browser. The require statement in Node.js is synchronous, dynamically bound, and can be called anywhere in the code, whereas the import statement is statically bound, must be at the top of the file, and is not asynchronous. Client-side JavaScript handles front-end UI interactions, while server-side JavaScript with Node.js processes and routes web service requests. Modules in Node.js can be core (built-in), local (created for your app), or third-party (from the community). Packages can be installed locally (accessible only within the app directory) or globally (accessible system-wide).

### Code Examples
```javascript
// Using require to import a module dynamically
const fs = require('fs');

// Using import statement (must be at the top of the file)
import express from 'express';

// Exporting a function in a local module
module.exports.myFunction = () => {
  console.log('This function is exported');
};
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| require() | Synchronously imports modules anywhere in the code |
| import | Statically imports modules at the top of the file |
| module.exports | Exports functions or values from a module |
| Core modules | Built-in Node.js modules with basic functionality |
| Local modules | Custom modules created for your application |
| Global install | Package accessible by all applications on the machine |
| Local install | Package accessible only within the application directory |

### Glossary
- **Node.js**: A JavaScript runtime built on Chrome's V8 engine for server-side programming.
- **require()**: A Node.js function to import modules synchronously and dynamically.
- **import**: An ES6 syntax for statically importing modules at the beginning of a file.
- **module.exports**: An object used to export functions or variables from a Node.js module.
- **Core modules**: Modules that come pre-installed with Node.js providing essential features.
- **Local modules**: Modules created by the developer for use within their application.
- **Global install**: Installing a package so it is available to all Node.js applications on the system.

### Summary
This module introduces the fundamentals of server-side JavaScript with Node.js, highlighting the differences between require and import statements, the types of modules available, and how packages can be installed and accessed. Understanding these basics is essential for building and managing backend applications effectively.