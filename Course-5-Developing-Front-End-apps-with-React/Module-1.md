 # Course 5: Developing Front-End Apps with React
## Module 1: Introduction to React, JSX Syntax, and Class Components

### Key Concepts
- React is an open-source JavaScript library for building dynamic, interactive front-end user interfaces.
- JSX (JavaScript XML) is a syntax extension that lets you write HTML-like code inside JavaScript.
- JSX requires a single parent tag wrapping multiple elements — either a real tag (`<div>`) or an empty fragment (`<>...</>`).
- A class component extends `React.Component` and must define a `render()` method that returns JSX.
- State in a class component is initialized in the constructor via `this.state = {...}` and accessed in JSX with `{this.state.variableName}`.
- Props are passed from parent to child as JSX attributes and accessed in the child via `this.props.variableName`.
- Event handling in class components is done by defining a method on the class and referencing it via `onClick={this.handleClick}`.
- Vite is the modern build tool used to scaffold and run React projects (faster than Create React App).
- Babel compiles JSX into plain JavaScript the browser can understand.
- ES6 (ECMAScript 6, released 2015) introduced modern JS syntax (`let`, `const`, classes, etc.) that React relies on heavily.

### Notes
React is a JavaScript library that makes it possible to build interactive, component-based user interfaces. Before writing any real components, this module lays the groundwork: how JSX syntax works, how class components are structured, and how a React project gets set up using Vite.

JSX lets you write markup that looks like HTML directly inside JavaScript. The browser can't run JSX natively — a tool called Babel compiles it into regular JavaScript function calls behind the scenes. One JSX rule to remember: a component can only return **one parent element**. If you have multiple sibling tags, you either wrap them in a real element like `<div>`, or use an empty fragment (`<>...</>`) when you don't want an extra wrapper element to show up in the actual DOM.

Class components are one way to define a React component. They are JavaScript classes that **extend** `React.Component` (making `React.Component` the superclass, and your component the subclass). Every class component must implement a `render()` method — this is what actually returns the JSX to be displayed. Inside a class component, you can manage **state**: a plain JavaScript object holding data that belongs to that component, initialized inside the constructor with `super()` called first (required, since it initializes the parent `Component` class before you can use `this`).

**Props** (short for properties) are how a parent component sends data down to a child component. They're written like HTML attributes on the child tag (`<Extra title={this.state.title} />`), and read inside the child using `this.props.title`. This is a one-way (parent → child) data flow — the child cannot modify props it receives.

**Event handling** in class components follows a familiar pattern: define a method on the class, then reference that method (without calling it) inside the JSX using an event attribute like `onClick`. This is different from a plain JS function call — you pass the function itself as a reference, so React calls it only when the event actually happens.

Finally, **Vite** is the tool used to create and run the React project itself. It's the modern replacement for Create React App, valued for its much faster dev server and build times, achieved by better use of native browser JS module handling. A new project is scaffolded using `npm create vite@latest`.

### Code Examples
```jsx
// JSX: wrapping multiple elements with a fragment
<>
  <h1>This is a heading tag</h1>
</>

// JSX: wrapping multiple elements with a real parent tag
<div>
  <h1>This is a heading tag</h1>
</div>
```

```jsx
// Basic class component
import React, { Component } from 'react';

export default class Extra extends Component {
  render() {
    return (
      <>
        <p>This is class component</p>
      </>
    );
  }
}
```

```jsx
// Class component with state
import React, { Component } from 'react';

export default class Extra extends Component {
  constructor() {
    super(); // must be called before using "this"
    this.state = { count: 0 };
  }
  render() {
    return (
      <>
        <p>The count is {this.state.count}</p>
      </>
    );
  }
}
```

```jsx
// Passing and receiving props between parent and child class components
// Parent: App.jsx
import React, { Component } from 'react';
import Extra from './Extra';

export default class App extends Component {
  constructor() {
    super();
    this.state = { title: "Manager" };
  }
  render() {
    return (
      <>
        <Extra title={this.state.title} />
      </>
    );
  }
}

// Child: Extra.jsx
<p>The count value is {this.props.title}</p>
```

```jsx
// Event handling in a class component
import React, { Component } from 'react';

class MyComponent extends Component {
  handleClick() {
    alert('Button clicked!');
  }
  render() {
    return (
      <div>
        <h1>Event Handling in Class Component</h1>
        <button onClick={this.handleClick}>Click Me</button>
      </div>
    );
  }
}

export default MyComponent;
```

```bash
# Scaffold a new React project with Vite
npm create vite@latest
```

### Cheat Sheet
| Concept | Syntax / Example | Description |
|---|---|---|
| Fragment | `<>...</>` | Wraps multiple JSX elements without adding an extra DOM node |
| Class Component | `class MyComponent extends Component { render() {...} }` | Defines a component using ES6 class syntax; must have a `render()` method |
| Constructor + super | `constructor() { super(); this.state = {...}; }` | Initializes state; `super()` must be called first |
| State | `this.state = { count: 0 }` | Holds the component's own data |
| Reading state | `{this.state.count}` | Displays state value inside JSX |
| Passing props | `<Extra title={this.state.title} />` | Sends data from parent to child as an attribute |
| Reading props | `{this.props.title}` | Accesses the received prop inside the child component |
| Event handling | `<button onClick={this.handleClick}>` | Passes a method reference to run on a user event |
| Create project | `npm create vite@latest` | Scaffolds a new React project using Vite |

### Glossary
- **App.jsx**: The root component of the React application.
- **Babel**: A tool used to compile JSX code so the browser can run it.
- **Class**: A template or blueprint for creating objects.
- **const**: Declares a constant whose value cannot be reassigned.
- **.eslintrc.cjs**: ESLint's configuration file; `.cjs` indicates a CommonJS module.
- **ECMAScript 6 (ES6)**: The 2015 JavaScript language specification that introduced modern syntax React relies on (classes, `let`/`const`, arrow functions, etc.).
- **Framework**: A comprehensive software development platform providing structure for building entire applications.
- **Front-end framework**: A framework focused specifically on building the user-facing side of web applications.
- **.gitignore**: Specifies which files/directories Git should ignore.
- **Hook**: A feature letting developers use state and other React features without writing class components.
- **index.html**: The entry point HTML file for a web application.
- **JSX (JavaScript XML)**: A syntax extension allowing HTML-like code inside JavaScript.
- **let**: Declares a block-scoped variable.
- **main.jsx**: The entry point file for the React application, where React mounts to the DOM.
- **Node modules**: Directory containing all npm/yarn-installed dependencies.
- **package.json**: File containing project metadata and dependency lists.
- **Public directory**: Contains static assets like HTML files, images, and fonts.
- **React**: An open-source JavaScript library for building dynamic, interactive user interfaces.
- **README.md**: File documenting the project — setup, usage, and general info.
- **src directory**: Contains the React application's source code.
- **Subclass**: A class that inherits from another class.
- **Superclass**: The class being inherited from.
- **this**: A reference to the current object/instance.
- **var**: A function-scoped (not block-scoped) variable declaration — legacy, largely replaced by `let`/`const`.
- **Vite**: A build tool that speeds up development by leveraging native browser JS module handling.
- **vite.config.js**: Configuration file for the Vite build tool.

### Summary
Module 1 covers the foundational syntax and setup needed before building real React apps: JSX rules (single parent element, fragments), how class components are structured with `render()`, state, and props, and how events are wired up using method references. It closes with Vite as the tool used to scaffold and run these projects, setting up everything needed to start building components in Module 2.