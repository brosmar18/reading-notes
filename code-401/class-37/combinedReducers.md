## Multiple Reducers Example

### Why create multiple Reducers?

Creating multiple reducers in Redux is advantageous for managing complex state structures in larger applications. Each reducer is responsible for handling a distinct segment of the app’s state, thereby organizing the codebase into manageable, modular parts. This separation makes the app easier to understand, maintain, and debug. By dividing the state management responsibilities among multiple reducers, developers can ensure that the logic for each part of the state is contained within is respective reducer, enhancing the scalability and maintainability of the app. 

### How Would you combine multiple reducers?

To combine multiple reducers in a Redux app, you use the `combineReducers` function provided by Redux. This function takes an object as an argument, where each key corresponds to a different part of the app’s state and each value is a reducer that manages that particular part. For example, if an app has user and tweets data, you might have `userReducer` and `tweetsReducer`. You combine them using `{ user: userReducer, tweets: tweetsReducer }`. The combined reducer that manages the overall app state, which each sub-render handler its specific slice of state independently. 

### How will you manage state as an immutable object? Why?

Managing state as an immutable object in Redux is crucial for predictability, debugging, and performance. When state is immutable, any changes to the state result in new objects rather than mutating existing ones. This approach avoids unintended side effects, which are common in large applications and can lead to difficult-to-track bugs. To manage state immutably, you would typically use JS operations that return new objects (like spreading an object with `...` or using array methods like ( `map()` and `filter()` that do not alter the original array). 

## Redux Docs: Using Combined Reducers

1. `combineReducers` is a utility function to simplify the most common use case when writing Redux reducers. It helps streamline the process of writing reducers that manage different slices of the state by combining them into a single reducer function. 
2. Explain how `combineReducers` assembles the new state tree
    
    `combineReducers` functions by calling each slice reducer contained within it with the corresponding slice of the app’s state and the current action. Each slice reducer independently assesses the action and may update its slice of the state accordingly. The `combineReducers` function then assembles these updated slices back into a new, single state object. This method ensures that each part of the state managed by a different reducer can respond to actions in a way that is both isolated from and consistent with other parts of the state, contributing to more predictable state management. 
    
3. How would you define initial state in an app using `combineReducers` ? 
    
    The initial state in an app using `combineReducers` can be defined in two primary ways: 
    
    - **Preloaded State:** When creating the Redux store with the `createStore` function, you can pass a `preloadedState` as the second argument. This is particularly useful for initializing the store with state that was persisted elsewhere, such as in the browser’s localStorage.
    - **Default State Values in Reducers:** Each reducer used with `combineReducers` can specify initial state by returning it when the state argument is undefined. This is typically done by setting default parameters in the reducers themselves. When `combineReducers` invokes each reducer for the first time, those that receive `undefined` as their slice of the state will return their initial state, establishing the initial state for their part of the overall state tree.
    
    These approaches hep ensure that the Redux store is correctly initialized with a coherent and expected state structure from the start. 
    

## Redux Docs: Combined Reducer Syntax

1. Why will you want to split your reducing functions as your app becomes more complex? 
    
    Splitting reducing functions into smaller, more focused reducers as your app grows in complexity is advantageous for several reasons. It helps manage state in a more organized and modular way, which simplifies maintenance and enhances scalability. Each reducer can focus on a specific part of the state, making the codebase easier to understand and debug. This approach also prevents any single reducer from becoming too large and unwieldy, which can lead to difficulties in managing state changes and tracking down bugs. Essentially, by dividing the state management responsibilities among different reducers, developers can ensure cleaner, more efficient code that aligns better with the principles of good software architecture. 
    
2. The `combineReducers` helper functions turns an object whose values are different reducing functions into a single reducing function you can pass to `configureStore` (or the legacy `createStore` method). 
3. What is a popular convention when naming reducers? 
    
    A popular convention when naming reducers is to align the names of the reducers with the slices of state they manage. This helps in easily identifying which reducer is responsible for which part of the state. For example, if a reducer manages the user information part of the state, it might be named `userReducer`. This naming convention ensures clarity and helps maintain a structured and intuitive understanding of the state management within the application. Additionally, in the use of `combineReducers`, the keys used for reducers in the object passed to it directly define the key names in the state object, which emphasizes the importance of thoughtful naming to accurately reflect the domain or data type they manage.

#### Citations
- [Multiple Reducers with Redux Reducers - Redux React Tutorial #4](https://www.youtube.com/watch?v=gBER4Or86hE)
- *Using combineReducers*. Retrieved from [Redux Documentation](https://redux.js.org/usage/structuring-reducers/using-combinereducers/)
- *combineReducers API*. Retrieved from [Redux Documentation](https://redux.js.org/api/combinereducers/)
