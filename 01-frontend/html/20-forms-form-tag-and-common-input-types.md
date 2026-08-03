# Forms: form Tag and Common Input Types

The form element wraps a set of controls submitted together, with action (where to send data) and method (GET or POST) attributes. Inside it, input handles most data entry, with the type attribute deciding its behavior - text, email, password, checkbox, radio, and more.

```html
<form action="/submit" method="POST">
  <input type="text" name="username">
  <input type="submit" value="Send">
</form>
```

**Key takeaway:** GET appends data to the URL (visible, bookmarkable); POST sends it in the request body.
