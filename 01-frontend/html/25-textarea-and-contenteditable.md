# Textarea and contenteditable

textarea provides a multi-line plain text input, sized with rows and cols or CSS. The contenteditable attribute, applied to almost any element, turns it into an editable region directly in the page - the basis for many rich text editors - though it needs careful sanitization before saving user input.

```html
<textarea rows="4" cols="40" placeholder="Your message"></textarea>
<div contenteditable="true">Edit me directly</div>
```

**Key takeaway:** contenteditable content must be sanitized before storage - it is a common XSS vector if trusted blindly.
