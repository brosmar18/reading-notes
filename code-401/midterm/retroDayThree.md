# Retro #3

## Progress

Today marked a challenging advancement in integrating real-time communication features in my application. The primary focus was incorporating Socket.io into the existing Express server, ensuring authentication requirements were met, and laying the groundwork for a real-time chat feature. I also populated the database with essential data to support the new functionalities and established a chatroom environment for users.

## Contributions

- **Socket.io Integration**: Successfully updated the Express server to support Socket.io, enabling real-time communication capabilities. This involved modifications to \`server.js` to incorporate Socket.io along with existing components like Express, Mongoose, and various routes. The integration ensures that the server can handle real-time events and maintain the integrity of the backend architecture.

- **Socket.io Authentication**: Implemented an authentication mechanism within Socket.io to verify connected Users. This was crucial for ensuring that only registered users have access to real-time features like chat. The authentication process, defined in \`server.js\`, utilizes `socket.handshake.auth` to validate usernames against the database, ensuring user legitimacy.

- **SocketClient Class**: Added a new `SocketClient` class to manage socket events more effectively. This class encapsulates the logic for handling socket connections, disconnections, and messages, providing a structured approach to manage real-time interactions.

- **Database updates**: Populated the Restaurant collection in the database and refined the User model to allow distinct roles of 'organizer' or 'attendee', enhancing data integrity. Also, updated User, Event, and Preferences collections with relevant data to support new functionalities.

- **Real-Time User Interaction**: Enhanced the socket.io logic to dynamically update connected users' list upon new user connections. This feature, as outlined in \`server.js\` and \`handler.js\`, provides a live view of users online, fostering a sense of community and interaction. 

- **Chatroom Setup**: Established a chatroom for user interactions, allowing users to join, send messages, and receive updates in real-time. This setup, detailed in \`server.js\` and \`handler.js\`, is pivotal in creating an engaging user experience and lays the foundation for future enhancements in chat functionalities.

## Challenges

- The biggest challenge was integrating Socket.io into the existing Express server. This was a new domain, requiring an understanding of real-time web technologies and REST APIs. Learning and implementing core Socket.io components (http, socket.io, server, and io) and integrating them with the existing server setup were critical yet challenging steps.

- Socket.io Authentication: Setting up authentication within the Socket.io framework posed a unique challenge. I delved into understanding \`socket.handshake.auth\` to ensure that only registered users could access the real-time features. This required a careful balance between security and functionality, ensuring that the authentication process aligns with the existing user registration logic in \`src/controllers/auth.js\` and \`routes/auth.js\`.

## Pull Request Link 
[Dev Day 03](https://github.com/Spots-LLC/spots-backend/pull/4)