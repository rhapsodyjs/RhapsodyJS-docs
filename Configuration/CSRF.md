# CSRF

If enabled, you must add a hidden field to your forms using the local `_csrf`m like this:

```html
	<form action="/enter" method="post">
		<label for="user">Username</label>
		<input type="text" name="user" id="user">
		<input type="hidden" name="_csrf" value="{{_csrf}}">
		<input type="submit">
	</form>
```