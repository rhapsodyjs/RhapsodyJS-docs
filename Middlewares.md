# Middlewares

A middleware is like a Controller action, but it receive three parameters:

* `req`: Request object
* `res`: Response object
* `next`: Calls the next route for the URL if the request passes the middleware

For example, a middleware that checks if a user is logged and, if so, take it to the info page, otherwise take it to the login page would look like this:

```js
	module.exports = function logged(req, res, next) {
	  if(typeof req.session.user !== 'undefined') {
	    next();
	  }
	  else {
	    res.redirect('/login');
	  }
	};
```