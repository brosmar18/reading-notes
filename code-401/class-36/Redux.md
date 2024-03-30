# Application State with Redux 

## What is the first principle of Redux? 

The first principle of Redux is having a single source of state. In a Redux app, the entire state of the app is stored in a single Object called the `store`. This means that all the data the app needs is centralized in one place, making it easier to manage, debug, and reason about. By consolidating the state into a single store, Redux ensures that there is a clear and consistent representation of the app's data at any given point in time. This approach simplifies the flow of data throughout the app and reduces the chances of inconsistencies or conflicts that can arise when managing state across multiple components or modules.

## What is a store and what do we use our reducers for within that Store?

A store is an object that holds the app’s state. It is created using the `createStore` function provided by the Redux library. The store is responsible for managing the state, dispatching actions, and allowing access to the current state via the `getState()` method. Reducers, on the other hand, are pure functions that specify how the state should be updated in response to dispatched actions. They take the current state and an action as arguments and return a new state object. Reducers are used within the store to handle different parts of the state and define the logic for modifying the state based on the received actions. By combining multiple reducers, you can create a modular and maintainable structure for managing complex application states.

## The `createStore` function provides three essential methods for interacting with the store:

- `getState()`: This method returns the current state object of the Redux store. It allows you to access the most up-to-date state in the app at any point in time.
- `dispatch(action)`: This method is used to dispatch an action to the Redux store. An action is a plain JS object that describes the type of action being performed and any associated data. When an action is dispatched, the store forwards it to the reducers, which then update the state accordingly.
- `subscribe(listener)`: This method allows you to register a callback function that will be invoked whenever the state in the Redux store changes. It is commonly used to update the UI or perform side effects in response to state changes. The `subscribe` method returns an unsubscribe function that can be called to remove the listener when it is no longer needed.

## Explain to a non-technical recruiter what `combineReducers()` does and why it is useful

`combineReducers()` is a utility utility function provided by Redux that simplifies the process of combining multiple reducers into a single reducer function. In non-technical terms, think of reducers as different departments in a company, each responsible for managing a specific part of the company’s data. `combineReducers()` acts as a manager that brings together all these departments and organizes them into a single, unified structure. It takes an object where the keys represent the different parts of the state and the values are the corresponding reducer functions. By using `combineReducers()`, you can split your Redux store into smaller, more manageable pieces, each handled by a separate reducer. This makes your code more modular, easier to understand, and simpler to test. It also allows different team members to work on different parts of the state independently, promoting better collaboration and maintainability.

## Things I want to know more about

One key area I want to explore is how Redux compares to other state management solutions like the Context API. It's my understanding that while Redux offers a centralized and scalable approach to state management, the Context API provides a more lightweight and component-centric solution. I'd like to delve deeper into the trade-offs and use cases for each approach to make informed decisions when architecting React applications. Understanding the strengths and limitations of both Redux and Context API will help me choose the most appropriate state management solution based on the specific requirements and scale of the project at hand.

#### Citation
[Fundamentals of Redux Course from Dan Abramov](https://egghead.io/courses/fundamentals-of-redux-course-from-dan-abramov-bd5cc867)
