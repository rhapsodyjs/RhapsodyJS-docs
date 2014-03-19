# Environments

In the `app/config/envs` are defined all the configurations for any of the environments of your app.
The `all.js` file contains configurations common for all the environments.

An environment file with all the options has the following form:

```js
var config = {
    host: 'localhost',
    port: 4242,

    database: {
        active: true, //If the app uses dabatase
        host: 'localhost',
        port: 27017,
        name: 'rhapsodyDB'
    },

    log: {
        level: 'debug', //For debug levels, see WolverineJS documentation: https://github.com/talyssonoc/wolverinejs
        output: '/home/rhapsody/log.log', //if undefined, will print to the terminal
        printStack: false, //If true, will print the error stack if an Error object is passed as argument in some log method
        printLevel: true, //If true, show the debug level before the message
        time: true //If true, shows the time the log was logged before the level name
    },

    socket: {
        active: true //If the app uses Socket. To set the socket behavior, see Socket in the Configuration session
    }
}
```