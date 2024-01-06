# Retro #1

## Progress 

Today, I made significant strides in developing the backend of my application. I focused on setting up the core architecture ensuring a solid foundation for further development.

## Contributions

- **Server Initialization and Configuration**: I set up the primary server files using Express (`index.js` and `server.js`), which included MongoDB connectivity and a `/` route as proof of life, along with error handlers (`404.js` and `500.js`).

- **Logging Mechanism**: I implemented a detailed logging system using Winston (`logger.js`), vital for tracking application behavior and debugging.

- **Database Models Development**: I created various MongoDB models (`User.js`, `Chat.js`, `Event.js`, `Message.js`, `Notification.js`, `Preferences.js`, and `Restaurant.js`). These models are crucial for data management in the application.

- **Testing**: I wrote comprehensive tests for the server and error handlers using Jest and Supertest (`404.test.js`, `500.test.js`, and `server.test.js`). These tests ensure that the server correctly handles routes and MongoDB connections, and properly logs both successful operations and errors. The tests for the 404 and 500 error handlers validate that the application responds appropriately to not found and internal server errors. The server tests cover route responses, MongoDB connection, and logging, ensuring the backend's reliability and functionality.

## Challenges

One of the major challenges faced today was ensuring comprehensive and thorough testing for the code developed. This was particularly evident while writing tests in `server.test.js`, where advanced testing strategies, such as mocking and utilizing the `MongoMemoryServer` dependency, were employed.

### Mocking `app.listen` due to Jest Warning

The challenge arose when confronted with a Jest warning:

> "Jest did not exit one second after the test run has completed."

This warning is indicative of asynchronous operations within the tests that were not terminated, preventing Jest from exiting cleanly. In testing our Express application, initiating the server to listen on a port, akin to its behavior in production or development environments, resulted in an open, ongoing asynchronous operation. This operation hindered Jest from closing post-test completion due to the server's continuous listening for incoming connections.

To resolve this, `app.listen` was mocked, simulating the server startup without actual activation. This method was crucial for testing key functionalities, like the MongoDB connection, under a controlled and isolated setup. By mocking, we avoided initiating a real server and, consequently, the creation of persistent asynchronous operations. This strategic move was instrumental in ensuring a smoother, more efficient testing process, allowing Jest to exit as expected after the completion of tests.
