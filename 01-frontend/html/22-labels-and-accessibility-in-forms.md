# Labels and Accessibility in Forms

Every input needs an associated label - either wrapping the input or linked via a matching for and id pair. This lets screen readers announce what a field is for, and lets users click the label text to focus the input, which is especially helpful for small checkboxes and radio buttons.

```html
<label for="email">Email</label>
<input type="email" id="email" name="email">
```

**Key takeaway:** A placeholder is not a substitute for a label - it disappears the moment the user starts typing.
