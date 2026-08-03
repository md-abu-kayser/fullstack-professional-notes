# Event Delegation Explained

Instead of attaching a listener to every individual child element, event delegation attaches a single listener to a shared parent and inspects event.target to determine which child was actually interacted with. This scales far better for dynamic lists where items are added or removed.

```javascript
list.addEventListener("click", (event) => {
  if (event.target.matches("li")) {
    console.log("Clicked:", event.target.textContent);
  }
});
```

**Key takeaway:** Delegation also automatically handles elements added to the DOM later - no need to re-attach listeners to new items.
