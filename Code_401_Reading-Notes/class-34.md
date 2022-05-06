# Authentication

## Bearer Tokens

- Bearer Tokens are created for users onces they have been authenticated after loggin in.
- These tokens can be thought of as a unique keycard that gives the user clearance to different levels of intel and abilities.
- When a request is made from the server, before it received the response of data, the users token must be authenticated first.

## [JWTs Explained](https://www.youtube.com/watch?v=926mknSW9Lo)

- JWT is a JSON Web Token
  - There are used to securely transfer info between two bodies.
  - It is compact data and can be sent via URL's, POST requests, and HTTP Header.
  - JWT's are *self contained* meaning it contains user info and avoids having to make a request to the database every time.
  - These are helpful for web authentication.
- JWT Structure
  - There is a *header*, *payload*, and *signature* section in a JWT.
  - The **header** is a JSON body object containing properties of `"alg"`, and `"typ"`.
  - The **payload** is JSON data containing *claims* which are user details or additional metadata.
  - Lastly there is the **signature** which includes the base64 header and base64 payload with a secret.
  - [Example below:](https://jwt.io/introduction)

  ```js
  HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  secret)
  ```

- Below is a diagram of how the flow of this works.
  - The client send user input sign in to authorization service.
  - That service then sends back a Token once cleared.
  - That is then used to make authorized requests to API

- ![Diagram](/img/JWT.png)
  - [Source](https://jwt.io/introduction)

## RBAC

- [role-based access control](https://www.csoonline.com/article/3060780/5-steps-to-simple-role-based-access-control.html)
- This is the idea that each user will have a *role*.
- That role will then determine what the user can access based on what route they are authorized to go.
- The benefits of RBAC is that it is more systematic and repeatable.
  - It lays out a clear visual of who has access to what and can make it easier to track down or find a specific set of users based on what CRUD action was performed.
