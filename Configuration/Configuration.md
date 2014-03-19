# Configuration

The configuration file `app/config/config.js` is where some global configurations are set.

## Environment

Should be a string, the name of the current environment of your app.
Initially RhapsodyJS creates two environment files for you (dev.js and prod.js, plus a all.js file with configurations common for all environments), but you can create infinite environment files inside the `env` folder and use its name (without the ".js") as a value to this option.

## Routes

It doesn't define the routes of your app (actually the routes are generated automatically, see the Controllers & Views session), but defines some configuration about routes, like:

* `mainController` Defines the first controller to be called when the user acess the root of your app
* `mainView` Defines the default view of a controller (can also be set in any controller) when user access the root of the controller
* `allowREST` If RESTful APIs should be generated for all the models. To a RESTful API work, this option must be true here and in the model. It this option is set to false, no RESTful URLs will be created for any model.