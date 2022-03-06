# CRUD

## Status Codes

- 100’s = Informational status codes.
- 200’s = Success status codes.
- 300’s = Redirection status codes if resource is not available.
- 400’s = Client error status codes meaning there is an issue that needs to be fixed on the **client** or **front-end** side.
- 500’s = Server error status codes meaning there is an issue that needs to be fixed on the **server** or **back-end** side.
- [HTTP Status Code](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/)
- What is a status code 202?
  - The request is valid and accepted but will process later.
- What is a status code 308?
  - This is a permanent redirection status and means you will need a new url to find the source.
- What code would you use if an update didn’t return data to a client?
  - 204, no content
- What code would you use if a resource used to exist but no longer does?
  - 410, gone
- What is the ‘Forbidden’ status code?
  - 403

## Build REST API With Node, Express, and MongoDB

- Why do we need to pull our MongoDB database string out of our server and put it into our .env?
  - It contains sensitive information that we do want to be displayed to everyone.
- What is middleware?
  - Another software that we use to mediate or use for a different task
- What does app.use(express.json()) do?
  - Parsing JSON data and requests
- What does the /:id mean in a route?
  - It means it is a parameter reached by request.params.id
- What is the difference between PUT and PATCH?
  - PUT will overwrite and push up the entire new code and update all data where PATCH is only partial data that is being modified.
- How do you make a default value in a schema?
  - By using the default keyword
- What does a 500 error status code mean?
  - It means that an error in the server has occurred.
- What is the difference between a status 200 and a status 201?
  - 201 is more specific about a successful update than 200.
