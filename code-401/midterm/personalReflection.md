## Final Reflection

**Describe your overall satisfaction level with your project results.** 
I am satisfied with the final outcome of my project. I feel proud of what I have built, particularly because I understand all of the concepts and tools used in my project, which demonstrates that I have learned a lot throughout this course.

**What went well and what did not?**
The use of GitHub Projects for project management went very well, enabling effective organization and tracking of tasks. However, time management posed a challenge owing to unforeseen personal events and an initially overambitious minimum viable product.

**How would you compare the outcome with your vision for the project?**
While the project fulfilled most minimum viable product (MVP) objectives like user authentication and an efficient backend infrastructure, it failed to actualize real-time notifications and matching Users to recommended events and restaurants in real-time via socket.io. This departed from my preliminary vision, underscoring the difficulties of scope regulation.

**Briefly describe your group dynamic for the week.**
As this was an individual project, the dynamic necessitated self-accountability. One major challenge entailed preserving momentum and resuming progress following unanticipated disruptions.

**Were there any problems that proved insoluble?**
I ran into various technical obstacles, including extensive testing and integrating complex capabilities like Socket.io. Despite posing difficulties initially, I managed to identify and implement suitable solutions congruent with my application's objectives.


**Describe at least one difficulty you faced during project week and how you dealt with it.**
One of the key challenges I faced was implementing a system to dynamically assign an "organizer" to each Event record created by a registered and logged-in user. This was a complex task that required altering the existing logic in the codebase to ensure that each event creation was correctly linked with the user as the organizer.

The solution involved enhancing the existing user verification process. I modified the middleware responsible for user authentication to effectively identify and confirm the user's identity based on their unique token. This step was crucial to ensure that the action of creating an event could only be performed by authenticated users.

Once the user's identity was verified and confirmed, I integrated this verification into the event creation process. The logic was updated so that every time an event was created, it automatically included the verified user's identifier as the event's organizer. This implementation was significant in maintaining data integrity and enforcing accountability for the events organized by users.

Tackling this challenge not only involved coding but also required a deep understanding of concepts like middleware, authentication, and database schema relationships. It was a valuable learning experience in applying these concepts to achieve the desired functionality while ensuring security and user responsibility.


**Describe at least one surprising success or failure you experienced during the week.**
A particularly surprising success during the project was overcoming the challenge of setting up authentication within the Socket.io framework. Initially, I anticipated significant difficulty in implementing this feature. 

Destipte multiple reviews of Socket.io documentation, I struggled to find a clear solution. A breakthrough occured when I reviewed a 'chat app' example in Socket.io documents. This example provided information on `socket.handshake.auth` logic. Basically, `socket.handshake.auth` allows the server to access authentication data that is sent automatically with each client connection. I can check if a socket is 'authenticated' by verifying data such as usernames and tokens inside the `socket.handshake.auth` object. 

**Describe changes you would make to your personal or team process that you can incorporate into your next team effort.**
In future projects, I plan to improve initial planning, including contingencies for unexpected events, and set a more realistic MVP to ensure achievable goals within the project timeline.

