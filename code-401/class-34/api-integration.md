# API Integration

## Review API Server Build

### Explain the difference between a query string parameter and a path parameter.

Query string parameters are used for filtering results returned by the API. For example, `http://amazingapi.com/api/v1/products?category=electronics` would retrieve all products where the category is 'electronics'. On the other hand, path parameters are part of the URL path itself and are typically used to identify a specific resource. The reading mentions using `/api/v#` where `#` is the version number, `/model` where 'model' is the name of the data model, and `/id` where `id` is the ID of a specific entity in the data model. So, the main difference is that query string parameters are used for filtering and refining results, while path parameters are used to specify the resource or entity being accessed or manipulated.

### What would our API URL with a path id parameter be given the following information:

- Domain: http://our-site.com
- API version: v3
- Model name: stuff
- ID: things

Based on the provided technical requirements and the given information, the API URL with a path ID parameter would be:

`http://our-site.com/api/v3/stuff/things`

This follows the standard routing structure mentioned in the reading:

- `/api/v#` where `#` is the version number of the API (in this case, `v3`)
- `/model` where 'model' is the name of the data model to operate on (in this case, `stuff`)
- `/id` where `id` is the ID of a specific entity in the data model (in this case, `things`)

So, putting together the given domain (`http://our-site.com`), API version (`v3`), model name (`stuff`), and ID (`things`), we arrive at the complete API URL: `http://our-site.com/api/v3/stuff/things`.

### We have created a dynamic API with an "interface". Describe how that interface works to a non-technical friend.

Imagine the dynamic API as a box that stores and manages different types of information. To interact with this box, you need to use a special set of rules, like a secret code. This code includes the box's location, the version of the code, the type of information you're looking for, and the specific item you want. The API is flexible and can handle various types of information, making it easy for people to interact with the stored data without needing to know the complex details behind the scenes.

## Review Auth Server Build

### Describe how you would use middleware to implement basic and bearer auth.

To implement basic and bearer auth using middleware, you would create separate middleware functions for each authentication method. The basic auth middleware would check for the presence of a valid username and password in the request headers, verify them against the user database, and either allow the request to proceed or return an error. The bearer auth middleware would check for the presence of a valid token in the request headers, verify its authenticity and expiration, and either allow the request to proceed or return an error. These middleware functions would be applied to routes that require authentication.

### Describe the handshake necessary to implement OAuth.

The OAuth handshake involves several steps. First, the user is redirected to the OAuth provider's login page. After successful login, the OAuth provider sends an authorization code back to the application. The application then exchanges this code for an access token by making a request to the OAuth provider's token endpoint. The OAuth provider verifies the code and returns an access token. The application can now use this access token to make requests to the OAuth provider's API on behalf of the user. The application should also create or update the user's account in its own database during this process.

### Describe how Role Based Access Control works to a non-technical friend.

Imagine you're running a company with different departments, and each department has specific responsibilities and access to certain information. In this scenario, Role Based Access Control (RBAC) is like giving each employee a special key card that grants them access to specific areas of the office based on their department. For example, a manager's key card would open more doors than an intern's. In the same way, RBAC assigns roles to users in a computer system, and each role has specific permissions. This way, the system ensures that users can only access the information and perform the actions they are allowed to, based on their role.

#### Citations

[Dynamic API Server](https://canvas.instructure.com/courses/7686890/discussion_topics/19474902?module_item_id=92931457)
[Authentication Server / Module](https://canvas.instructure.com/courses/7686890/discussion_topics/19474902?module_item_id=92931457)
