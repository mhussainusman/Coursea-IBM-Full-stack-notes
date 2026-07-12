# Course 5: Developing Front-End Apps with React
## Module 2: React Components — Types, State, Props, and Lifecycle

### Key Concepts
- React components modularize the UI into reusable, independent parts.
- Four main types of React components: functional, class, and higher-order components (three categories in practice, HOCs being a pattern built on top of the other two).
- Class components extend `React.Component` and manage state and lifecycle.
- Props pass data from parent to child components.
- State holds a component's own data and triggers a re-render whenever it changes.
- Component lifecycle has three phases: mounting, updating, unmounting.

### Notes
React components let developers break the UI into independent, reusable pieces instead of one giant tangled page. This modular approach makes code easier to organize, test, and maintain. React has a few types of components: **functional components** (plain JS functions returning JSX), **class components** (ES6 classes extending `React.Component`), and **higher-order components** — a pattern where a function takes a component and returns an enhanced version of it, rather than a component type on its own.

Class components manage three things internally: **state** (their own data), **lifecycle events** (hooks into when the component is created, updated, or destroyed), and **methods** (functions defined on the class, e.g. event handlers). This module builds directly on Module 1's class component basics.

**Props** carry data down from a parent component to a child, enabling communication through the component tree. **State** is different — it's a plain JavaScript object holding a component's *own* current data. Whenever `this.setState(...)` is called to update state, React automatically re-renders that component to reflect the new data. The key distinction: props come from **outside** (parent-controlled, read-only in the child), state is **owned and controlled by the component itself**.

The **component lifecycle** describes the sequence a class component goes through:
- **Mounting** — the component is created and inserted into the DOM for the first time. `componentDidMount()` runs right after this happens — commonly used for things like initial data fetching.
- **Updating** — the component re-renders due to changed state or props.
- **Unmounting** — the component is removed from the DOM. `componentWillUnmount()` runs just before this — used for cleanup (e.g. clearing timers, canceling subscriptions).

Understanding these phases matters for controlling *when* certain code should run — you don't want to fetch data on every re-render, only once on mount, for example.

### Code Examples
```jsx
// Class component managing both state and props, with a lifecycle method and event handler
import React, { Component } from 'react';

class Greeting extends Component {
  constructor(props) {
    super(props); // pass props to the parent Component class
    this.state = { message: 'Hello' };
  }

  componentDidMount() {
    console.log('Component mounted'); // runs once, right after first render
  }

  handleClick = () => {
    this.setState({ message: 'Hello, ' + this.props.name }); // updates state -> triggers re-render
  };

  render() {
    return (
      <div>
        <h1>{this.state.message}</h1>
        <button onClick={this.handleClick}>Greet</button>
      </div>
    );
  }
}

export default Greeting;
```

### Cheat Sheet
| Concept | Syntax / Example | Description |
|---|---|---|
| Class Component | `class MyComponent extends React.Component {}` | Defines a component with state and lifecycle methods |
| Props | `<ChildComponent propName={value} />` | Passes data from parent to child component |
| State | `this.state = { key: value }` | Holds component data that triggers re-rendering |
| Update state | `this.setState({ key: newValue })` | Updates state and schedules a re-render |
| Event Handling | `<button onClick={this.handleClick}>` | Responds to user interactions like clicks |
| Lifecycle Methods | `componentDidMount()`, `componentWillUnmount()` | Manage component phases: mount, update, unmount |

### Glossary
- **React Component**: A modular, reusable piece of UI in React.
- **Class Component**: A React component defined as a JavaScript class extending `React.Component`.
- **Props**: Properties passed from a parent component to a child component.
- **State**: An object that holds data that influences a component's rendering; owned by the component itself.
- **Lifecycle**: The phases a component goes through from creation to removal — mounting, updating, unmounting.
- **Higher-Order Component (HOC)**: A function that takes a component and returns a new, enhanced component.

### Summary
Module 2 builds on class component fundamentals from Module 1, going deeper into state, props, and the component lifecycle. It clarifies the difference between state (component-owned, triggers re-renders) and props (parent-supplied, read-only), and introduces the three lifecycle phases — mounting, updating, unmounting — needed for controlling when component logic runs.