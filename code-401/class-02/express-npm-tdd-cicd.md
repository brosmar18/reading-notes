# Express, NPM, TDD, CI/CD

## Intro to Node.js and Express

1. Explain middleware, answer as though I were a non-technical recruiter. 

    Middleware is like a series of checkpoints that web requests go through before reaching their final destination. Imagine you're at an airport; before boarding your flight, you go through various stages like security checks, passport control, and boarding pass verification. Each of these stages ensures everything is in order before you proceed. In web apps, middleware functions similarly, performing specific tasks or checks at each stage before the final web page is presented to the user.

2. Express is the most popular ______. 

    Express is the most popular Node web framework. 

3. Express is "unopinionated". What does that mean? 

    It means that it doesn't force developers to follow a specific way of doing things or use certain tools. It's like being given a toolbox without a manual; you have the freedom to use the tools in any way you see fit. This flexibility allows developers to structure their apps in the way they prefer and choose the best tools for their specific needs. However, this also means that developers need to make more decisions on their own, as there isn't a "one-size-fits-all" approach.

4. What is a module and why is modularity useful to use as developers? 

    A module is like a self-contained unit or building block of code that can be easily plugged into a larger system. Think of it as a puzzle piece in a jigsaw puzzle. Each piece has a specific shape and image, and when combined with other pieces, it forms a complete picture. In software development, modules allow us to break down complex apps into smaller, manageable parts. This modularity is useful because it makes our code more organized, easier to understand, and allows for reusability. Instead of rewriting the same code multiple times, we can write it once in a module and reuse it wherever needed.

## NPM 

1. What version of npm are you running on your machine?

    I am running npm version 9.8.1


2. What command would you type to install a library/package called ‘jshint’ into your node project?

    To install `jshint` package into a node project, I would use the following command: 

    `npm install jshint`

## TDD

1. Explain why tests are important. Please explain as though I were your non technical elder.

    Imaging you're knitting a sweater. Before finishing the entire sweater, you'd want to periodically check if you're following the pattern correctly, if the size is right, and if there are any holes or mistakes. In software development, tests serve a similar purpose. They allow developers to check if the "sweater" (software) they're "knitting" (coding) is shaping up correctly. By running these tests, they can catch any "holes" or errors early on, ensuriing the final product is error-free. 


2. What are three expected benefits of testing

    - Fewer Mistakes: Testing helps  catch and fix errors early, leading to software with fewer issues. 

    -  Saves Time Later: While testing might take a bit of time upfront, it saves more time in the end by avoiding big problems later. 

    - Better Quality Software: With regular testing, the final software works better and is more reliable


3. Name at lest 2 individual pitfalls and at least 2 team pitfalls commonly encountered while writing tests.

    **Individual Pitfalls**

    - Forgetting to run tests frequently. 
    - Writing tests that are too large or coarse-grained. 

    **Team Pitfalls**

    - Partial adoption, where only a few team members use TDD. 

    - Poor maintenance of the test suite, often leading to a suite that takes too long to run. 