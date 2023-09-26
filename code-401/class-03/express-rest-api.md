# Express REST API

## Review: ES6 Classes

1. Classes are a template for creating ____.

    Classes are a template for creating objects. They encapsulate data with code to work on that data. 


2. Can a class declaration be hoisted?

    No, class declarations are not hoisted. They have the same temporal dead zone restricftions as let or const and behave as if they are not hoisted. 


3. How would you describe a constructor and contextual “this” to a non-technical friend?

    Image you are in a car factory. The factory has a blueprint for making a car. This blueprint includes all the steps and parts needed to assemble the car, like wheels,doors, and the engine. Think of the constructor as the part of the blueprint that specifies how to start building the car. It ensures that each car starts with four wheels, two doors, and one engine. It's like the basic setup for every car that gets built. Now, imagine that while the car is being built, it needs to be referred to. Instead of saying "the car being built right now,", we just say "this car.". So, "this" is like a nickname for the car being built at the moment. When the blueprint says "put an engine in this car," it means put an engine in the car currently being assembled. 