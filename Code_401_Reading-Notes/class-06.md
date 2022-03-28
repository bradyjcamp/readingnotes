# Authentication

## Securing Passwords

- A great way to protect passwords is through hash algorithms such as **Cryptographic hash algorithms**
  - Hashing will essential convert your plaintext password into hashes and so if the database is stolen or corrupted, they will only take the hashed version of the password.

### Problems with Cryptographic Hash Algorithm

- There are different types of hacking attacks and one is a **Brute Force Attack**.
  - This attack is when a hacker uses a word dictionary to input different types and repeat that over and over again.
- Another type is **Hash Collision Attack**.
  - Sometimes there will be two hashed versions of two different passwords that match. In this case, hackers will try and find those similarities to exploit.
- Then there is **BCrypt**.
  - [It is slow but strong.](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)
  - Bcrypt uses a technique called *Key Stretching*.
    - Key stretching increases the amount of time and space it takes to test each key or password.
    - It receives an input key and then generates a stretched cipher called an [*enhanced key*](https://en.wikipedia.org/wiki/Key_stretching)

## Basic Access Authentication

- This is a method for an HTTP agent to provide a username and password when [making a request](https://en.wikipedia.org/wiki/Basic_access_authentication).
- This process does not require cookies or login pages because is uses fields in the HTTP header.

> For example, if the browser uses Aladdin as the username and open sesame as the password, then the field's value is the Base64 encoding of Aladdin:open sesame, or QWxhZGRpbjpvcGVuIHNlc2FtZQ==. Then the Authorization header field will appear as:
Authorization: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ==

## [Authentication Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html)

- Authentication verifies a user. Authorization allows that user to continue.
- There are many different types of authentication for the World Wide Web and other applications.
- Some guidelines include ensuring a username is unique, and making sure the password is strong and not too short or too long.
- There are all sorts of different ways to ensure security on private data or information such as:
  - Change password security
    - This is when you are prompt to confirm and enter your old password before creating a new one.
  - TLS Client Authentication
    - This is when the server and the browser or client meet to confirm they each have corresponding info.
  - Multi-factor Authentication
  - And other programs like:
    - OAuth
    - OpenId
    - SAML
    - FIDO

#### Other Sources

- [bcrypt docs](https://www.npmjs.com/package/bcrypt)