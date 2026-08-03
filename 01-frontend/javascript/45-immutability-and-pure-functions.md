# Immutability and Pure Functions

A pure function always returns the same output for the same input and causes no side effects (no mutating arguments, no network calls, no writing to outer variables). Favoring immutable updates (creating new objects/arrays instead of mutating existing ones) makes state changes predictable and much easier to debug, especially in UI frameworks like React.

```javascript
// Impure - mutates the input
function addItem(list, item) { list.push(item); return list; }

// Pure - returns a new array
function addItemPure(list, item) { return [...list, item]; }
```

**Key takeaway:** React and Redux both rely on reference equality checks for performance - mutating state directly instead of replacing it can silently break re-rendering.
