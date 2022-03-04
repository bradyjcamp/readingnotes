# Authentication

- What is OAuth?
  - >OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential.
  - [What is OAuth](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)
- Give an example of what using OAuth would look like.
  - If you were to use your Facebook login info to login to Spotify or you Google account info to login to a different website.
- How does OAuth work? What are the steps that it takes to authenticate the user?
  - The website the user is on connects to a different website to receive the users identity.
  - That different site then generates a one-time token and secret.
  - The initial site then gives this token and secret to the client software.
  - The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).
  - If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.
  - The user approves (or their software silently approves) a particular transaction type at the first website.
  - The user is given an approved access token (notice it’s no longer a request token).
  - The user gives the approved access token to the first website.
  - The first website gives the access token to the second website as proof of authentication on behalf of the user.
  - The second website lets the first website access their site on behalf of the user.
  - The user sees a successfully completed transaction occurring.
  - OAuth is not the first authentication/authorization system to work this way on behalf of the end-user. In fact, many authentication systems, notably Kerberos, work similarly. What is special about OAuth is its ability to work across the web and its wide adoption. It succeeded with adoption rates where previous attempts failed (for various reasons).
  - [Directly from site](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html)
- What is OpenID?
  - It is a different security technology and the key difference is that it is more about *authentication* rather than *authorization*

## Authorization and Authentication Flows

- What is the difference between authorization and authentication?
  - Authentication is about confirming the users info and authorization is about allowing access.
- What is Authorization Code Flow?
  - It exchanges an authorization code for a token.
  - [Authorization Code Flow](/img/auth-sequence-auth-code.png)
  - [Source](https://auth0.com/docs/get-started/authentication-and-authorization-flow/authorization-code-flow)
- What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
  - Extra layer of protection when using a public client
  > The PKCE-enhanced Authorization Code Flow introduces a secret created by the calling application that can be verified by the authorization server; this secret is called the Code Verifier. Additionally, the calling app creates a transform value of the Code Verifier called the Code Challenge and sends this value over HTTPS to retrieve an Authorization Code.
  - [Source](https://auth0.com/docs/get-started/authentication-and-authorization-flow/authorization-code-flow-with-proof-key-for-code-exchange-pkce)
- What is Implicit Flow with Form Post?

 >Implicit Flow with Form Post flow uses OIDC to implement web sign-in that is very similar to the way SAML and WS-Federation operates. The web app requests and obtains tokens through the front channel, without the need for secrets or extra backend calls. With this method, you don’t need to obtain, maintain, use, and protect a secret in your application.

- [Source](https://auth0.com/docs/get-started/authentication-and-authorization-flow/implicit-flow-with-form-post)
- What is Client Credentials Flow?
  - This is when the client itself passes along its ID and Secret to authenticate itself to get a token.
- What is Device Authorization Flow?
  - The Client ID passes itself to initiate the authorization process.
- What is Resource Owner Password Flow?
  - Users credentials stored and used for authorization.