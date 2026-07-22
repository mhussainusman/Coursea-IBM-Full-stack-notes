# Course 5: Developing Front-End Apps with React
## Module 3: In-depth Understanding of Advanced React Functionality

### Key Concepts
- Redux elements: actions, store, reducers
- Application state management via a single store
- Reducers as pure functions updating state
- Synchronous vs asynchronous operations in Redux

### Notes
Redux centralizes the entire application's state in a single object called the store, rather than using individual component states. Actions are objects that communicate what data needs updating to the store. Reducers are pure functions that take the current state and an action, then return a new updated state without mutating the original. This approach ensures predictable state changes. Synchronous operations in Redux run sequentially, waiting for each to finish before starting the next, while asynchronous operations can run in parallel, improving efficiency in handling tasks like API calls.

### Code Examples
```javascript
// Action example
const incrementAction = {
  type: 'INCREMENT',
  payload: 1
};

// Reducer example
function counterReducer(state = { count: 0 }, action) {
  switch(action.type) {
    case 'INCREMENT':
      return { count: state.count + action.payload };
    default:
      return state;
  }
}

// Store creation (using Redux library)
import { createStore } from 'redux';
const store = createStore(counterReducer);

// Dispatching an action
store.dispatch(incrementAction);
console.log(store.getState()); // { count: 1 }
```

### Cheat Sheet
| Term/Command | What it does |
|---|---|
| Action | Object describing what change to make |
| Store | Holds the entire application state |
| Reducer | Pure function that updates state based on action |
| Dispatch | Sends an action to the store |
| Synchronous | Operations run one after another |
| Asynchronous | Operations can run in parallel |

### Glossary
- **Action**: A plain object that describes a change to be made in the state.
- **Store**: The centralized object holding the entire state of the application.
- **Reducer**: A pure function that takes the current state and an action, returning a new state.
- **Synchronous Operation**: Tasks executed sequentially, one after the other.
- **Asynchronous Operation**: Tasks that can be executed concurrently without waiting for others to finish.

### Summary
This module introduces Redux as a state management tool that uses actions, a centralized store, and reducers to update application state predictably. Understanding the difference between synchronous and asynchronous operations is key to managing data flow efficiently in Redux-based applications.