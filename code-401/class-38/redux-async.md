# Redux: Asynchronous Actions

## Async

1. Why use Redux middleware? 
    
    Redux middleware is used to extend Redux’s capabilities, enabling custom behavior during the dispatch process of an action. Middleware acts as a third-party extension point between dispatching an action and the moment it reaches the reducer. In practice, middleware allows for handling async operations, logging, crash reporting, and more sophisticated interactions with dispatched actions that are not possible with Redux alone. For instance, async API calls, require middleware like Redux Thunk because Redux itself only supports sync data flow. Middleware effectively bridges this gap by intercepting actions and potentially altering them, delaying them, replacing them, or performing additional logic like API calls before passing the actions on to the reducers. 
    
2. Consider the Redux Async Data Flow Diagram. Describe the flow in your own words. 
    
    Everything begins with the user interacting with the UI, such as clicking a “Deposit $10” button. This interaction triggers an event handler. The event handler then dispatches an action to the store. However, because this action involves async logic (like calling an API), it doesn’t go directly to the reducer. The dispatched action is intercepted by middleware before it can reach the reducers. Middleware is configured to handle specific types of actions, particularly those that involve async work. The middleware, upon recognizing an action that requires an API call, performs this async operation. Once the API call is completed and a response is received, the middleware dispatches a new action to the store, this time with the data fetched from the API. This new action is processed by the reducers, which update the state based on the action type and payload. The updated state is reflected back in the UI, which may show the new balance after the deposit action is completed. 
    
3. How are we accommodating async in our Redux App? 
    
    The documentation provides an example of a ToDo App. Async operations are managed by using middleware, specifically Redux Thunk. Thunks allow us to write functions that can perform async requests and interact with the Redux store. For instance, thunks are used to fetch todo items from a server and post new todos. These thunk functions are dispatched just like regular actions, but they handle the async logic internally. Once the async operation is complete, the thunk dispatches another action with the payload containing data received from the API, which the reducer then uses to update the state. This approach of using thunks separates the concerns of API interactions and state management, thereby keeping the Redux store logic clean and focused solely on state updates.  
    

## Thunk Middleware

1. Why would you need `redux-thunk` middleware? 
    
    You would need redux-thunk middleware to handle side effects in your Redux application, especially for complex synchronous logic that requires access to the store and for async logic, such as API requests. The middleware provides a way to write action creators that can perform these tasks and dispatch actions based on the outcome of these operations. 
    
2. Redux thunk middleware allows you to write action creators that return a function instead of an action. 
3. Describe how any return value from the inner thunk function will be made available. 
    
    Any return value from the inner thunk function will be available as the return value of `dispatch` itself. This means when you dispatch a thunk, you can expect the return value to be whatever the thunk returns. This feature is particularly useful for orchestrating async control flows, where thunk action creators can dispatch other thunks and return Promises to wait for each other’s completion. It allows developers to build complex logic that can handle async operations in a predictable manner, chaining promises and actions in a sequence that respects the asynchronous nature of the tasks being performed.

#### Citations 
- [reduxjs/redux-thunk](https://github.com/reduxjs/redux-thunk)
- [Redux Fundamentals, Part 6: Async Logic and Data Fetching](https://redux.js.org/tutorials/fundamentals/part-6-async-logic)


