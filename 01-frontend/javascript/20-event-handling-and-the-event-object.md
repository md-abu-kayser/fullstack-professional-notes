# Event Handling and the Event Object

addEventListener attaches a handler function to an element for a given event type. The handler automatically receives an event object with details like target (what triggered it), type, and methods like preventDefault to stop default browser behavior.

```javascript
form.addEventListener("submit", (event) => {
  event.preventDefault();
  console.log(event.target);
});
```

**Key takeaway:** Prefer addEventListener over inline onclick attributes or the older onclick property - it supports multiple listeners on the same element.
