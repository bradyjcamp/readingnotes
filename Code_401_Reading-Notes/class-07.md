# Bearer Authorization

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

## Bearer

- How does JWT work?
  - When a user is trying to access a protected route, the JWT is sent.
  - Typically it is sent in the **Authorization** header using the **Bearer** schema.

```js
Authorization: Bearer <token>
```
