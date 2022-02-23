# API's

- What does REST stand for?
  - **Representational state transfer**
- REST APIs are designed around a ____.
  - *Resources* - which are any sort of data, object, or service that can be access by the client
- What is an identifier of a resource? Give an example.
  > A resource has an identifier, which is a URI that uniquely identifies that resource. For example, the URI for a particular customer order might be: https://adventure-works.com/orders/1
  - [Source](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)
- What are the most common HTTP verbs?
  - **GET**, **POST**, **PUT**, **PATCH**, and **DELETE**.
- What should the URIs be based on?
  - the resource or *nouns*
- Give an example of a good URI.
  > [https://adventure-works.com/orders](https://adventure-works.com/orders)
  - [Source](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)
- What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
  - Bad things
    - This is a large number of small resouces.
- What status code does a successful GET request return?
  - HTTP status code 200 (OK).
- What status code does an unsuccessful GET request return?
  - HTTP status code 406 (Not Acceptable).
- What status code does a successful POST request return?
  - HTTP status code 201 (Created).
- What status code does a successful DELETE request return?
  - HTTP status code 204 (No Content)

## RegExr

- How would you match a phone number from your city using RegEx?

## Things I want to know more about

- RegExr