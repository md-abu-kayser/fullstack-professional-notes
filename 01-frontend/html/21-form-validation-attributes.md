# Form Validation Attributes

HTML provides built-in validation without JavaScript: required marks a field mandatory, pattern enforces a regex, and min, max, minlength, and maxlength constrain values or length. Browsers block submission and show a native error message when these fail.

```html
<input type="text" required minlength="3" pattern="[A-Za-z]+" title="Letters only">
```

**Key takeaway:** Built-in validation improves UX instantly but should still be backed by server-side validation.
