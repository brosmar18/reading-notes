# Components Based UI

## React Quick Start

### What are the building blocks of a React app?  

The building blocks of a React app are components. Components are independent and reusable bits of code that serve as the foundation of a React app. They are like JavaScript functions that return HTML via a render function. Components can be as small as a button or as large as an entire page's layout. Each component encapsulates its own structure, behavior, and style, allowing complex apps to be built from these modular and manageable pieces. Components can be nested within other components, enabling a hierarchical structure that mimics the UI's structure. This modular approach makes the development process more manageable and the application easier to understand and scale.


### What is the difference between an HTML element and a React component?  

HTML elements are the basic building blocks of web pages, defined by HTML standard tags. They directly represent the markup that will be rendered in the browser. React components, on the other hand, are more abstract. They are JavaScript functions or classes that return React elements (which can represent HTML elements or other components). React components can include additional logic, state management, and lifecycle methods, allowing for more complex and dynamic behaviors than static HTML elements. Essentially, while HTML elements are the final output to the browser, React components are the higher-level building blocks that produce and manage these elements.


### What is JSX and why do we use it?  

JSX is a syntax extension for JavaScript, commonly used with React to describe what the UI should look like. It resembles HTML in appearance, but it allows JavaScript to be mixed with HTML-like text. JSX makes it easier to write and understand the structure of the UI components in a way that is similar to writing HTML templates, but with the full power of JavaScript. JSX gets compiled to JavaScript, allowing developers to write elements and components in a more readable and expressive syntax, enhancing the development experience. It streamlines the process of building complex UI structures, as it visually represents the UI components while being backed by JavaScript functionalities.


### Describe the process of embedding JavaScript expressions in JSX.  

In JSX, JavaScript expressions can be embedded by enclosing them in curly braces `{}`. This allows for the dynamic content within the JSX markup. For example, variables, functions, and other JS expressions can be included directly in the JSX structure. When the JSX is processed, these expressions are evaluated and the results are inserted into the rendered output. This feature enables the creation of dynamic and interactive user interfaces, where the content can change in response to user actions or other events.


### Does React or JSX have any special features for iteration or conditional logic?

React and JSX use standard JavaScript features for iteration and conditional logic. For iteration, such as rendering a list of items, the JavaScript's `map` function is commonly used. This function can transform each item in an array into a JSX element, effectively rendering a dynamic list of elements. For conditional logic, React utilizes the standard JS conditional statements like `if-else` or ternary operations `(condition ? true : false)`. These can be used to conditionally render components or elements based on certain conditions, making the UI dynamic and responsive to different states or user interactions.


### How does React know to respond to a user’s inputs?  

React responds to user inputs through a mechanism called event handling. React components can define event handlers for various user interactions, such as clicks, form submissions, or keyboard events. These event handlers are functions written in JavaScript and are linked to specific events in the JSX. For example, a button in JSX can have an `onClick` attribute with a function that defines what happens when the button is clicked. React's synthetic event system ensures that these handlers work consistently across different browsers. When a user interacts with the UI, the corresponding event handler is triggered, allowing React to respond accordingly, such as updating the component's state or triggering a UI change.


### What word indicates that a React component manages data with a Hook?

In React, the word that indicates a component is managing data with a Hook is `useState`. This is a built-in Hook provided by React that allows functional components to have state. When a component uses `useState`, it declares a state variable and a function to update it. For instance, `const [count, setCount] = useState(0);` declares a state variable `count` and a function `setCount` to update it. The use of `useState` and other Hooks like `useEffect` and `useContext` signifies that a component is managing its data or side effects through these Hook mechanisms.


### How can two React components share data?  

Two React components can share data through a concept known as "props" (short for properties) and state lifting. When components need to share data, the common practice is to "lift the state up" to their closest common ancestor. This means moving shared state to a parent component. The parent component then passes the data down to the children components as props. Props are read-only and allow data to flow from parent to child components, ensuring that child components react to changes in the shared state. This approach maintains a unidirectional data flow, which is a key principle in React, making the data flow easier to understand and debug.

## Render and Commit 

### What are the three steps of refreshing a React UI?

The process of refreshing a React user interface involves three primary steps: Trigger, Render, and Commit. First, the Trigger step involves initiating the rendering process. This can occur when a component is rendered for the first time (initial render) or when a component's state or the state of its ancestors has been updated. The second step, Render, is where React calls the components to determine what should be displayed. This includes creating new DOM nodes during the initial render or calculating changes during subsequent renders. Finally, in the Commit step, React applies these determined changes to the DOM. For the initial render, it uses methods like `appendChild()` to add new elements, and for re-renders, it applies the necessary updates to the existing DOM structure.

### How do you trigger updates to a component after the initial render?

Updates to a React component after the initial render are typically triggered by changing the component's state or its props. This is often done through the `setState` function for class components or the state update function returned by the `useState` hook in functional components. For example, calling `this.setState({ value: newValue })` in a class component or `setValue(newValue)` in a functional component using `useState` will trigger a re-render. These state changes tell React that the component and its children need to be re-rendered with the updated state. This process is part of React's reactive design, where UI updates are automatically managed in response to state changes.

### Does React recreate DOM nodes on every rerender?

React does not recreate all DOM nodes on every re-render. It uses a process called reconciliation to efficiently update the DOM. During the rendering phase, React calculates the changes that need to be made to the actual DOM. It compares the newly rendered output (virtual DOM) with the previous render and determines the minimal set of changes required to update the actual DOM. Only the parts of the DOM that have changed are updated, not the entire tree. This selective updating minimizes the performance impact and makes the updates efficient. For example, if only the text content of an element changes, React will only update the text content of that specific DOM node rather than recreating the entire node.

### After React has updated the DOM, what still needs to happen before the user sees the change?

After React has updated the DOM, the final step before the user sees the change is the browser's repainting on the screen, also known as the 'browser paint' step. This is a process managed by the browser, not by React. Once React commits the changes to the DOM, the browser then needs to reflect these changes visually on the screen. This involves the browser's layout and painting processes, where it calculates the layout of the updated elements and then redraws the affected portions of the screen. This painting process is what ultimately makes the changes visible to the user. It's important to note that this step happens automatically and is managed by the browser after React has done its part in updating the DOM.

## Things I want to konw more About


#### Citations
- React Team. (n.d.). *Quick Start – React*. React. Retrieved from [https://react.dev/learn](https://react.dev/learn)

- React Team. (n.d.). *Render and Commit – React*. React. Retrieved from [https://react.dev/learn/render-and-commit](https://react.dev/learn/render-and-commit)
