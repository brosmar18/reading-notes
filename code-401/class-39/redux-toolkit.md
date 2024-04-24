## Redux Toolkit (RTK)

1. What concerns are addressed by Redux Toolkit? 
    
    Redux Toolkit addresses several common concerns associated with using Redux in development projects. Firstly, it simplifies the configuration of a Redux store, which can be overly complex. Secondly, it reduces the need to add numerous additional packages to make Redux functional for common use cases. Lastly, it tackles the problem of Redux necessitating too much boilerplate code. By providing a set of tools and utilities that abstract and streamline these aspects, Redux Toolkit makes it easier and quicker to integrate Redux into your projects, allowing developers to focus more on developing their application logic rather than setup and configuration. 
    
2. What does `configureStore()` do? 
    
    `configureStore()` is a function provided by Redux Toolkit that simplifies the setup of the store in Redux. It wraps the Redux `createStore` function but abstracts away the common configuration options and provides good defaults. This includes automatically combining slice reducers, adding Redux middleware (with `redux-thunk` included by default), and enabling support for the Redux DevTools extension. The function helps in setting up a Redux store with less boilerplate and more sensible defaults, making the process more efficient and less error-prone. 
    
3. How would I use `createSlice()`? 
    
    `createSlice()` is a function in Redux Toolkit that significantly reduces the Redux boilerplate needed for creating reducers and actions. To use `createSlice()`, you define a slice object that includes a name, an initial state, and an object of reducer functions that correspond to the types of actions that might be dispatched. `createSlice()` automatically generates action creators and action types that correspond to the reducers defined in the slice. This allows developers to write concise, readable code that manages the state and handles updates. The simplicity of managing state with reducers, without manually creating each action type of creator, showcases the practicality and efficiency of `createSlice()` in application development. 
    

## MobX

1. What MobX?
    
    MobX is a state management library designed to be simple, scalable, and highly efficient, commonly used in combination with React to manage state in applications. It operates on principles that automate state management tasks, ensuring tat updates are propagated correctly across the application’s UI without the need for explicit state manipulation by the developer. MobX utilizes concepts such as observables, computed values, and actions to automatically handle dependencies and updates in a predictable manner. 
    
2. How does MobX make it “impossible” to produce an inconsistent state? 
    
    MobX ensures a consistent state by treating application state like a spreadsheet, where any change in the underlying data automatically updates all derived values without manual intervention. This is achieved through a mechanism where dependencies are tracked dynamically and only the necessary computations are re-executed in response to specific changes in state. This automated dependency management prevents the state from becoming out-of-sync with the UI or other parts of the application, thus eliminating inconsistencies. 
    
3. How would we build a reactive user interface? 
    
    To build a reactive user interface with MobX, you would use the `observer` higher-order component from the `mobx-react-lite` package to wrap your React components. This approach automatically subscribes the component to relevant pieces of the application state, ensuring that it re-renders whenever the data depends on changes. This means that changes in the state due to actions are immediately reflected in the UI without explicit calls to update functions, thereby making the entire UI reactive to state changes. 
    

## Tutorial

1. What take-away(s) did this tutorial provide? 
    
    The tutorial highlighted how Redux Toolkit simplifies Redux codebases. It reduces boilerplate code through utilities like `createSlice()`, which consolidates traditional Redux flow into fewer, more manageable lines of code. The integration of Redux with React Hooks, especially through the Redux Toolkit, is showcased. This integration allows for a more intuitive and streamlined way of connecting Redux state to React components, aligning Redux more closely with modern React development practices. RTK Query, as introduced in the tutorial, extends Redux ToolKit’s capabilities into efficient server-side state management. It automates the handling of loading states, caching, and data fetching. 
    

### Citaitons

- [Redux Toolkit Introduction](https://redux-toolkit.js.org/introduction/getting-started)
- [MobX Getting Started](https://mobx.js.org/getting-started.html)
- [Learn Modern Redux with Mark Erikson](https://www.youtube.com/watch?v=9zySeP5vH9c)