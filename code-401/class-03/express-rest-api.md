# Express REST API

## Review: ES6 Classes

1. Classes are a template for creating ____.

    Classes are a template for creating objects. They encapsulate data with code to work on that data. 


2. Can a class declaration be hoisted?

    No, class declarations are not hoisted. They have the same temporal dead zone restricftions as let or const and behave as if they are not hoisted. 


3. How would you describe a constructor and contextual “this” to a non-technical friend?

    Image you are in a car factory. The factory has a blueprint for making a car. This blueprint includes all the steps and parts needed to assemble the car, like wheels,doors, and the engine. Think of the constructor as the part of the blueprint that specifies how to start building the car. It ensures that each car starts with four wheels, two doors, and one engine. It's like the basic setup for every car that gets built. Now, imagine that while the car is being built, it needs to be referred to. Instead of saying "the car being built right now,", we just say "this car.". So, "this" is like a nickname for the car being built at the moment. When the blueprint says "put an engine in this car," it means put an engine in the car currently being assembled. 

## Using Express Routing

1. Within Express, what does routing refer to?

    Routing in Express refers to the definition of application endpoints (URIs) and how they respond to client requests. The routing methods of the Express app correspond to HTTP methods, and they specify a callback function (sometimes called "handler functions") that is called when the app receives a request to that specified route (endpoint) and HTTP method. 

2. What is the difference between a route path and a route method?

    A **route method** is derived from one of the HTTP methods and is attached to an instance of the Express class. It determines the HTTP method for which the route will be applied. For exmple, `app.get()` handles GET requests, and `app.post()` handles POST requests. 

    A **route path**, in combination with a request method, defines the endpoints at which requests can be made. Route paths can be strings, string patterns, or regular expressions. They define the part of the URL which the route should apply to. 


3. When is it appropriate to add next as a parameter to a route handler and what must you do if next has been passed to your middleware as a parameter?

    It is appropriate to add `next` as a parameter to a route handler when you have more than one callback function as arguments. With multiple callback funcions, it is important to provide `next` as an argument to the callback function and then call `next()` within the body of the function to hand off control to the next callback. This is used to pass control to the next middleware function in the stack. 

## Express Routing

1. What is an Express Router?

    An Express router is like a mini-Express application without views or settings, but with the routing APIs like `.use`, `.get`, `.param`, and `route`. It allows you to create modular and maintainable code by organizing related routes and middleware into a single router object. 


2. By what mean do we initialize express.Router() in an express server?

    To initialize `express.Router()`, you call an instance of the `express.Router()` and apply routes to it. Then, you tell your app to use those routes. For example: 

    ```js
        var router = express.Router();
        router.get('/', function(req, res) {
            res.send('Home Page');
        });
        app.use('/', router);
    ```

    This code snippet creates a router, defines a GET route on it, and then applies the router to the application. 


3. What do we use route middleware for?

    Route middleware in Express is used to perform operations before a request is processed. It can be used for various tasks like checking if a user is authenticated, logging data for analytics, or any other operations that should be executed before responding to a request. Middleware is defined using `router.use()` and will be applied to all the requests that come into the app for that instance of Router. It can also be used to validate parameters using `.param()` middleware. 

    