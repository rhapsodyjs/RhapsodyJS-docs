# Environments

In the `app/config/envs` are defined all the configurations for any of the environments of your app.
The `all.js` file contains configurations common for all the environments.

An environment file with all the options has the following form:

```js
var config = {
    host: 'localhost',

    http: {
        port: 4242,
        socket: true
    },

    https: {
        enabled: true,
        port: 4243,
        socket: true
    },

    methodOverride: {
        enabled: true,
        attributeName: 'newMethod',
    },

    database: {
        enabled: true, //If the app uses dabatase
        host: 'localhost',
        port: 27017,
        name: 'rhapsodyDB',
        username: undefined,
        password: undefined
    },

    log: {
        level: 'debug', //For debug levels, see WolverineJS documentation: https://github.com/talyssonoc/wolverinejs
        output: '/home/rhapsody/log.log', //if undefined, will print to the terminal
        printStack: false, //If true, will print the error stack if an Error object is passed as argument in some log method
        printLevel: true, //If true, show the debug level before the message
        time: true, //If true, shows the time the log was logged before the level name
        silent: false
    },

    routes: {
        //Controller used when access the app's root
        mainController: 'main',

        //View used when the user doen't specify it
        mainView: 'index',

        //If must be created REST routes for models
        allowREST: true
    },

    enableCompression: true,

    generateClientModels: true
}
```