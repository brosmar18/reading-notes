# Access Control (ACL)

## 5 Steps to RBAC

1. What is Role Based Access Control (RBAC) and why do we care?

    Role-Based Access Control (RBAC) is a method of regulating access to computer or network resources based on the roles of individual users within an organization. RBAC is significant because it simplifies the management and assignment of access rights, reducing the risk of unauthorized access and potential security breaches. By defining roles based on job functions and assigning permissions to these roles rather than to individual users, RBAC ensures that users only have access to the information and resources that are necessary for their duties. This approach not only enhances security but also improves operational efficiency and compliance with regulatory requirements, as it is easier to audit and manage.

2. Describe a Role/Permission hierarchy that you might implement using RBAC.

    In implementing RBAC, you might establish a hierarchy that includes roles such as "Administrator", "Manager", "Employee", and "Guest". Each role would have permissions that align with job responsibilities. For instance, an "Administrator" might have full system access, including the ability to add or remove users and change the system settings. A "Manager" might have permissions to view and edit all documents within their department, approve requests, and generate reports. An "Employee" could be granted access to view and edit documents pertinent to their specific projects and tasks. Lastly, a "Guest" might only have read access to certain non-sensitive documents. This hierarchy ensures that access is appropriately tiered, with each subsequent role inheriting the permissions of the preceding role, plus additional privileges as needed for their specific function.

3. What approach might you take to implement RBAC?

    To implement RBAC, you would start by conducting a thorough inventory of all systems and resources to determine what needs to be protected. Next, analyze job functions within the organization to define roles that encapsulate specific access needs. Once roles are established, assign users to these roles based on their job functions. It's crucial to avoid making one-off changes for individual users, as this can lead to inconsistencies and security gaps. Instead, adjust roles or create new ones as necessary to fit unique requirements. Finally, establish a routine for auditing the system to ensure that roles and access rights remain aligned with users' needs and that no unnecessary permissions are granted, maintaining a secure and efficient access control system.


## wiki - RBAC

1. If Authentication is “you are who you say you are,” what is Authorization?

    Authorization is the process that comes after authentication, determining what an authenticated user is allowed to do. It involves granting or denying rights to access resources and perform actions within a system or network. While authentication verifies identity, authorization checks the permissions of a user based on predefined policies. This ensures that users can only perform actions and access data that they are permitted to, according to their assigned roles or attributes.

2. Name three primary rules defined for RBAC.

    The three primary rules defined for RBAC are role assignment, role authorization, and permission authorization. Role assignment ensures that a user can only access permissions through assigned roles. Role authorization requires that a user's activated role must be authorized for them, preventing users from assuming unauthorized roles. Permission authorization ensures that a user can only perform actions if those actions are authorized for the user's active role, maintaining secure and appropriate access.

3. Describe RBAC to a non-technical friend.

    Imagine you're at a music festival with different areas like the stage, VIP lounge, and backstage. RBAC is like the wristbands you wear that show which areas you can enter. Just like wristbands are given based on the type of ticket you bought, in RBAC, users are given 'digital wristbands' or roles based on their job. These roles determine what information they can see or what they can do on a computer system. It's a way to make sure everyone only gets into the 'areas' they're supposed to, keeping things orderly and secure.

 ## RBAC Tutorial 

1. What Are access rights Associated with? The User? or The Role? Explain.

   In Role-Based Access Control (RBAC), access rights are associated with roles rather than individual users. This means that permissions to access certain resources within a system are not granted directly to a user; instead, they are assigned to a role that a user can then be given. Roles are defined based on job functions within the organization, and users are assigned to these roles. By doing so, RBAC ensures that users only have access to the information and resources necessary for their specific job functions, which streamlines the management of access rights and helps maintain a more secure and orderly access environment.

2. Access Rights, or Authorization, is activated after a user successfully does what?

    Access rights, or authorization, in the context of RBAC, are activated after a user successfully authenticates themselves. Authentication is the process by which a system verifies the identity of a user, typically through credentials like a username and password. Once the system confirms the user's identity, it then proceeds to authorize the user based on the roles previously assigned to them. This authorization step is where the system determines what the user is allowed to do within it, such as accessing specific files, databases, or applications, based on the permissions tied to their role. 

3. Explain how RBAC might benefit a business.

   RBAC can benefit a business in several ways. Firstly, it enhances security by ensuring that users only have access to the resources necessary for their roles, reducing the risk of internal and external breaches. Secondly, it simplifies the management of user permissions, making it easier for administrators to add, remove, or change roles as well as audit permissions across the organization. This can lead to increased operational efficiency, as less time is spent on managing individual user permissions. Additionally, RBAC supports compliance with regulatory requirements by providing a clear framework for access control that can be easily documented and reviewed. Overall, RBAC helps in creating a more secure, manageable, and compliant IT environment.

#### Citations
- [5 Steps to Simple Role-based Access Control](https://www.csoonline.com/article/555873/5-steps-to-simple-role-based-access-control.html)
- [Role-Based Access Control](https://en.wikipedia.org/wiki/Role-based_access_control)
- [Role Based Access Control](https://www.youtube.com/watch?v=C4NP8Eon3cA)
