# Socket

All the Socket behavior are defined here.

The `app/config/socket.js` is a function that receives the io object (an instance of [Socket.io](http://socket.io/)) as parameter, so you can create the rooms, messagens, listeners and so on.

All the socket [advanced options](https://github.com/LearnBoost/Socket.IO/wiki/Configuring-Socket.IO) must also be done here using the method `io.set(property, value)`.