# Buttons: button vs input type=submit

button can contain other HTML like icons or spans, and defaults to type submit inside a form unless specified otherwise - a common source of accidental form submissions. input type submit is simpler but can only show plain text as its label.

```html
<button type="button">Just a click, no submit</button>
<button type="submit">Submit the form</button>
```

**Key takeaway:** Always set an explicit type on button inside forms to avoid unintended submissions.
