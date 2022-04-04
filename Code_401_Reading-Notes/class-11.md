# Event Driven Applications

- Event Driven programming helps our code to avoid issues of complexity and collision.
- When thinking of examples of events we will look at the web browser.
  - When a user clicks a button or when a key is pressed, and event is triggered.
  - Two key aspects in our code that monitor these events are **Event Handlers** and a **Main Loop**.
    - An event handler takes in a callback function that is called when an event is triggered.
    - The main loop will listen for an event to be triggered and then calls that event handler.

## EventEmitter

- Node.js provides us with a module called EventEmitter.
- See the below example of how to require in and use the module:

```js
const EventEmitter = require('events').EventEmitter;
const myEventEmitter = new EventEmitter;
```

- The first method to add that is good practice would be a function to listen for when a *user joined*.

```js
const EventEmitter = require('events').EventEmitter;
const chatRoomEvents = new EventEmitter;

function userJoined(username){
  // Assuming we already have a function to alert all users.
  alertAllUsers('User ' + username + ' has joined the chat.');
}

// Run the userJoined function when a 'userJoined' event is triggered.
chatRoomEvents.on('userJoined', userJoined);
```

- The next step would be to make sure that our chat room triggers a `userJoined` event whenever someone logs in so that our event handler is called.  
  - EventEmitter has an `emit` method that we we use to trigger the event. We would want to trigger this event from within a login function inside of our chatroom module.

```js
function login(username){
  chatRoomEvents.emit('userJoined', username);
}
```
