# Access Control

- **RBAC**
  - [role-based access control](https://www.csoonline.com/article/3060780/5-steps-to-simple-role-based-access-control.html)
  - This is the idea that each user will have a *role*.
  - That role will then determine what the user can access based on what route they are authorized to go.
  - The benefits of RBAC is that it is more systematic and repeatable.
    - It lays out a clear visual of who has access to what and can make it easier to track down or find a specific set of users based on what CRUD action was performed.
  - Alternatives to RBAC
    - **ACL**
      - ACL stands for **Access Control Lists**.
      - This splits up access to a specific object
      > As a simple example, an ACL could be used to allow users from one department to make changes to a document, while only allowing users from other departments to read the document.
      - [CSO](https://www.csoonline.com/article/3060780/5-steps-to-simple-role-based-access-control.html)
    - **ABAC**
      - ABAC stands for **Attribute-based access control**
      - This splits up access based on what attributes are tied to an object.
    - Using these other methods will work but can expand the complexity and require more effort when keeping track of permissions
  **RBAC implementation**
    - **Inventory your systems**
      - Determine what data or resources need controlled access.
    - **Analyze work force and create roles**
      - You need to determine different roles for different levels of users.
      - Each user needs to have a specific set of roles tied to them.
    - **Assign those roles**
    - **Never make one-off changes**
      - The more unsusual cases you have, the messy the structure of roles and access will be.
      - Keep them concise and limit the amount of sinlge user specific roles.
    - **Audit**
      - It is important to review roles and reassess what users roles are and if they need to be updated.
- [RBAC Tutorial](https://www.youtube.com/watch?v=C4NP8Eon3cA)
