# Message Queues

## Socket.io Chat Example

- First step is to install all the dependencies and bring them into your `index.js` file like so:

[Snippet provided by this link](https://socket.io/get-started/chat/)

```js
const express = require('express');
const app = express();
const http = require('http');
const server = http.createServer(app);

app.get('/', (req, res) => {
  res.send('<h1>Hello world</h1>');
});

server.listen(3000, () => {
  console.log('listening on *:3000');
});
```

- This creates the server and has it running on `PORT 3000`
- We have also created an http request route using `app.get`.
- After creating the HTML side, we now have to integrate **socket.io**

### Socket.io Integration

[Snippet provided by this link](https://socket.io/get-started/chat/)

```js
const express = require('express');
const app = express();
const http = require('http');
const server = http.createServer(app);
const { Server } = require("socket.io");
const io = new Server(server);

app.get('/', (req, res) => {
  res.sendFile(__dirname + '/index.html');
});

io.on('connection', (socket) => {
  console.log('a user connected');
});

server.listen(3000, () => {
  console.log('listening on *:3000');
});
```

- You will need to connect the server side of socket.io to the client and listen for a connection like we showed above.
- This will allow the server to be alerted and display the message that *a user connected*.
- Then you can set up broadcasting to `emit` a message to those connected.

```js
io.on('connection', (socket) => {
  socket.broadcast.emit('hi');
});
```

## Rooms

- Server sockets can be defined and split up into rooms.

[Snippet provided by this link](https://socket.io/docs/v4/rooms/)

```js
io.on("connection", (socket) => {
  socket.join("some room");
});
```

- To then emit to specific rooms use the following code:

```js
io.to("some room").emit("some event");
```

[Here is a link to the Emit Cheatsheet](https://socket.io/docs/v4/emit-cheatsheet/)
