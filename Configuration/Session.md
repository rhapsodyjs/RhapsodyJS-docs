# Session

In the `app/config/session.js` file you will have all the options for the use of sessions in your app.

This file can have the following options:

```js
{
    sessionIDKey: 'sessionID', //The id of the session on the browser of the client
    cookieSecret: 'rhapsodyCookieSecret', //The secret to use signed cookies. If "undefined", the cookies will be unsigned
    sessionSecret: 'rhapsodySessionSecret', //The secret used to protect the cookie key of the session in the browser of the client
    maxAge: 60000 //The max age of the cookies. If "undefined", the cookies will never expire
}
```