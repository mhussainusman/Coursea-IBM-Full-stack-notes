# Course 6: Developing Back-End Apps with Node.js and Express
## Module 2: Asynchronous I/O with Callback Programming

### Key Concepts
- Asynchronous network operations use callback functions to avoid blocking JavaScript execution.
- Callback functions pass messages from Node.js modules back to the main application after receiving responses.
- Nested callbacks can be complex and hard to debug, leading to inversion of control and trust issues.
- Promises provide a cleaner way to handle time-consuming asynchronous operations.
- JSON.parse() and JSON.stringify() are essential methods for working with JSON data in Node.js.

### Notes
Asynchronous I/O in Node.js allows operations like network requests to run without stopping the rest of the program. This is achieved by using callback functions, which are invoked once the operation completes. However, callbacks can become nested and difficult to manage, a problem known as "callback hell." This also introduces inversion of control, where the flow of the program depends on external code, which can cause trust and maintenance issues. Promises offer a more manageable alternative by representing future values and enabling chaining. Working with JSON is common in back-end apps, and Node.js provides built-in methods to parse JSON strings into objects and convert objects back to JSON strings.

### Code Examples
```javascript
// Example of a simple asynchronous callback
function fetchData(callback) {
  setTimeout(() => {
    const data = { id: 1, message: "Hello" };
    callback(data);
  }, 1000);
}

fetchData((result) => {
  console.log("Received data:", result);
});

// Using JSON methods
const jsonString = JSON.stringify({ name: "Node.js" });
const jsonObject = JSON.parse(jsonString);
console.log(jsonObject.name); // Output: Node.js
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| callback function | Function passed as an argument to handle async results |
| Promise | Object representing eventual completion or failure of async operation |
| JSON.parse() | Converts JSON string into a JavaScript object |
| JSON.stringify() | Converts JavaScript object into a JSON string |

### Glossary
- **Callback function**: A function passed to another function to be executed after an asynchronous operation completes.
- **Inversion of control**: A situation where the flow of a program is controlled by external code, often leading to complexity.
- **Promise**: An object that represents the eventual completion or failure of an asynchronous operation.
- **JSON**: JavaScript Object Notation, a lightweight data interchange format.

### Summary
This module covers how asynchronous I/O operations in Node.js use callback functions to prevent blocking the main thread. It highlights challenges with nested callbacks and introduces promises as a better alternative. Additionally, it explains how to work with JSON data using built-in parsing and stringifying methods.