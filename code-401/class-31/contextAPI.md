# Context API

## Choosing the State Structure

### Summarize the five principles of structuring state

1. **Group Related State**: When two or more state variables are always updated together, it's advisable to merge them into a single variable. This approach helps in maintaining synchronization between related pieces of state, making the component easier to manage.

2. **Avoid Contradictions in State**: State should always be structured to prevent pieces of state from contradicting each other. Contradictory state can lead to bugs and inconsistencies in the application's behavior. Ensuring that the state remains consistent and unambiguous can reduce errors.

3. **Avoid Redundant State**: If certain information can be derived from existing state variables or component props during rendering, it should not be stored as a separate piece of state. Redundant state increases the complexity of state management and the risk of inconsistencies.

4. **Avoid Duplication in State**: Duplication occurs when the same data is represented in multiple state variables or nested within objects, making it challenging to keep them synchronized. Reducing duplication helps in maintaining a single source of truth for each piece of data in the application.

5. **Avoid Deeply Nested State**: Deeply hierarchical or nested state structures make updates cumbersome and error-prone. Favoring a flatter state structure simplifies the process of updating state and can make the code easier to understand and maintain.

## Passing State Deeply with Context

### What problem do Contexts aim to solve?

Contexts in React aim to solve the problem of "prop drilling", which occurs when data needs to be passed through multiple layers of components. Prop drilling can make the code verbose, hard to maintain, and difficult to scale. Context provides a way to share values like theme data or user information between components without having to manually pass props through every level of the component tree, thus simplifying the data flow in complex applications.

### What is one technique to try before useContext?

Before resorting to `useContext`, React documentation suggests trying to pass data through props as the first approach. This method keeps the data flow explicit and makes it clear which components use which data. If passing props becomes too cumbersome due to multiple layers of intermediate components that don't use the data themselves, another recommended technique is to extract components and pass JSX as children to them. This reduces the number of layers between the component specifying the data and the component that needs it, potentially eliminating the need for `useContext` in simpler scenarios.

### What hook complements useContext for complex applications?

For complex applications, the `useReducer` hook often complements `useContext`. `useReducer` is useful for managing complex state logic that involves multiple sub-values or when the next state depends on the previous one. By combining `useContext` with `useReducer`, developers can manage and pass down complex application states more efficiently, making the state accessible to deeply nested components without prop drilling, while keeping the state logic organized and centralized.

## Things that I want to know more about

I'm interested in learning more about how Context can be leveraged for optimizing state flow in large-scale applications. I'm curious about the best practices for combining `useContext` with `useReducer` for managing complex, intertwined state logic. Additionally, I want to understand the impact of Context on performance and how it compares with other state management libraries or patterns in React. 


#### Citations
- *Choosing the State Structure*. React. Retrieved from [https://react.dev/learn/choosing-the-state-structure](https://react.dev/learn/choosing-the-state-structure)

- *Passing Data Deeply with Context*. React. Retrieved from [https://react.dev/learn/passing-data-deeply-with-context](https://react.dev/learn/passing-data-deeply-with-context)

