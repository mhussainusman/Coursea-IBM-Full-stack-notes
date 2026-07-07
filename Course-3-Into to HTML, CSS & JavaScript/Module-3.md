# Course 3 - Module 3: JavaScript Programming for Web Applications

### Key Concepts
- JavaScript is a scripting language that adds dynamic content to web pages.
- Variables are declared using `let` or `const` and take their type from the assigned value.
- Program execution is controlled by statements like If…Then…Else, Switch, For loops, and While loops.
- Functions are blocks of code that can be called from anywhere in the script.
- Prototypes allow adding methods and properties to all instances of an object.
- Client-side scripts enhance interactivity by working with HTML documents via the script tag.
- The Document Object Model (DOM) is the programming interface between HTML and JavaScript.
- APIs are used to access and manipulate HTML DOM elements in web pages.

### Notes
JavaScript enables developers to create dynamic and interactive web pages. Variables are declared with `let` or `const`, and their types are inferred from the assigned values. Control structures such as If…Then…Else, Switch, For loops, and While loops manage the flow of the program.

Functions encapsulate reusable blocks of code that can be invoked anywhere in the script. JavaScript objects can be extended by modifying their prototypes, allowing new methods and properties to be shared across all instances.

Client-side scripting involves embedding JavaScript within HTML documents using the `<script>` tag, either inline or by linking external files. The DOM represents the HTML document as a tree of objects, which JavaScript can access and manipulate to change the page content dynamically.

APIs provide standardized ways to interact with the DOM and other web technologies, enabling developers to build rich, interactive user experiences.

### Code Examples
```javascript
// Variable declaration
let name = "Alice";
const age = 30;

// Control structure example
if (age > 18) {
  console.log("Adult");
} else {
  console.log("Minor");
}

// Function example
function greet(person) {
  return `Hello, ${person}!`;
}

console.log(greet(name));

// Prototype example
function Person(name) {
  this.name = name;
}

Person.prototype.sayHello = function() {
  console.log(`Hi, I'm ${this.name}`);
};

const person1 = new Person("Bob");
person1.sayHello(); // Hi, I'm Bob
```

### Cheat Sheet
| Concept | Syntax / Example | Description |
|---|---|---|
| Variable | `let x = 5;` / `const y = "text";` | Declare variables with let or const |
| If Statement | `if (condition) { ... } else { ... }` | Conditional execution |
| For Loop | `for (let i=0; i<5; i++) { ... }` | Loop with counter |
| While Loop | `while (condition) { ... }` | Loop while condition is true |
| Function | `function name(params) { ... }` | Define reusable code blocks |
| Prototype | `Constructor.prototype.method = function() {}` | Add methods/properties to all instances |
| Script Tag | `<script src="file.js"></script>` | Include JavaScript in HTML |
| DOM Access | `document.getElementById("id")` | Access HTML elements via JavaScript |

### Glossary
- **JavaScript**: A scripting language used to create dynamic content on web pages.
- **Variable**: A named storage for data values.
- **Function**: A block of code designed to perform a particular task.
- **Prototype**: An object from which other objects inherit properties and methods.
- **Client-side scripting**: Code that runs in the user's browser to create interactive web pages.
- **DOM (Document Object Model)**: A programming interface for HTML and XML documents representing the page structure as objects.
- **API (Application Programming Interface)**: A set of functions and protocols for building and interacting with software applications.

### Summary
This module introduced JavaScript fundamentals for web development, including variables, control flow, functions, prototypes, and client-side scripting. It emphasized how JavaScript interacts with the DOM and uses APIs to create dynamic, interactive web pages.