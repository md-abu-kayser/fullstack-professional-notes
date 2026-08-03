# The DOM: Selecting and Manipulating Elements

The DOM is the browser's in-memory tree representation of HTML. querySelector/querySelectorAll select elements using CSS selector syntax, while properties like textContent, innerHTML, and classList let you read or change what is rendered.

```javascript
const card = document.querySelector(".card");
card.classList.add("active");
card.textContent = "Updated";
```

**Key takeaway:** Prefer textContent over innerHTML when inserting plain text - innerHTML with untrusted input is a direct XSS risk.
