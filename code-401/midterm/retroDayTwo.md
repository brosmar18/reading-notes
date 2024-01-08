# Retro #2

## Progress

Today was a productive day in the backend development of the application. My work primarily revolved around enhancing the authentication logic, building out essential routes, and implementing robust testing for these functionalities.

## Contributions

### Authentication Logic and Routes
- Implemented **Authentication Logic** in `auth.js`, including user registration and login. This involved integrating bcrypt for password hashing and JWT for token generation.
- Developed **Auth Routes** (`src/routes/auth.js`) for user registration (`/register`) and login (`/login`), providing the necessary endpoints for user authentication.

### Testing Authentication Logic
- Wrote tests for registration and login logic in `register.test.js` and `login.test.js`. These tests ensure the reliability of our authentication process, including user existence validation and error handling.

### Authorization Middleware
- Created `verifyToken` middleware in `verifyToken.js` to handle user authorization. This middleware validates JWTs, ensuring secure access to protected routes.

### CRUD Operations Handling
- Built a generic **CRUD class** (`Collection.js`) to streamline the creation, reading, updating, and deletion of database records. This class enhances the modularity and maintainability of our codebase.

### Routes Development
- Developed **User Routes** in `src/routes/user.js`, enabling operations like fetching, updating, and deleting user records.
- Implemented **Event Routes** (`routes/event.js`), providing endpoints for event management, including creation, retrieval, updating, and deletion of events.
- Created **Preferences Routes** (`routes/preferences.js`) to manage user preferences, allowing creation, retrieval, updating, and deletion.
- Established **Restaurant Routes** (`routes/restaurant.js`) to handle restaurant-related operations, offering endpoints for adding, fetching, updating, and removing restaurant records.

## Challenges

## Dynamic Assignment of "Organizer" in Event Records

One of the key challenges I faced today was implementing a logic to dynamically assign an "organizer" to an Event record when a registered and logged-in user creates an event. This task was intricate due to the need to modify the existing logic in the codebase to correctly associate a user with the "organizer" field during event creation. 

#### Implementation in `verifyToken.js`
The solution involved leveraging the existing `verifyToken` middleware to ensure that only authenticated users could perform this action. In `verifyToken.js`, I implemented code to find a user based on their ID, obtained from the verified JWT token:

```javascript
const user = await User.findById(verified.id);
if (!user) return res.status(401).send('User Not Found');
req.user = user;
```

#### Integration in Event Routes
With the user information available in the request (`req.user`), I updated the event creation logic in `routes/event.js`. 

```js
// Create an event
router.post('/event', verifyToken, async (req, res) => {
    const userId = req.user.id;
    const eventDetails = { ...req.body, organizer: userId };
    const newEvent = await eventCollection.create(eventDetails);
    res.status(201.json(newEvent));
});

```

This implementation ensures that every event created is automatically assigned an organizer corresponding to the authenticated user, thereby maintaining data integrity and enforcing user accountability for the events they organize. 

The challenge was not just in writing the code but in understanding and applying the concepts of middleware, JWT authentication, and Mongoose schema relationships to achieve the desired functionality. 

## Pull Request Link 
[Dev Day 02](https://github.com/Spots-LLC/spots-backend/pull/3)