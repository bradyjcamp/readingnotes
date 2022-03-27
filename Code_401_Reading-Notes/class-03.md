# Express REST API

## Classes

> [Classes are templates for creating objects](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)

- They are considered to be *special functions*
- Demo Code:

```js
class Rectangle {
  constructor(height, width) {
    this.height = height;
    this.width = width;
  }
}
```

- Classes must be defined before they are constructed or a new instance is created
- The `constructor` method creates the object parameters of the class.
- `this` keyword is referencing the object or class.
- You can also create **subclasses** of a class:

```js
class Animal {
  constructor(name) {
    this.name = name;
  }

class Dog extends Animal {
  constructor(name) {
    super(name);
  }

```

- [Code Source](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
- `**super**` in the extended class above refers to the original paramaters in the constructor of the original class function.

## Express Routing

- **Routing** is a reference to the endpoints in an application.
- That references is a request from the client and it gets a response back.
- There are different request methods for routing like app.get and app.post.
  - These requests will have what is called a handler function for each specific route.
- Routes also have **parameters**
  - These parameters help guide the request to the client so it receives specified data based on the route parameters.

```js
Route path: /flights/:from-:to
Request URL: http://localhost:3000/flights/LAX-SFO
req.params: { "from": "LAX", "to": "SFO" }
```

- [Code Source](https://expressjs.com/en/guide/routing.html)

- Route Handlers are used to chain paths by using `app.route()`.

```js
app.route('/book')
  .get((req, res) => {
    res.send('Get a random book')
  })
  .post((req, res) => {
    res.send('Add a book')
  })
  .put((req, res) => {
    res.send('Update the book')
  })
```

- You can then bring it in to another file:

```js
const express = require('express')
const router = express.Router()
```
