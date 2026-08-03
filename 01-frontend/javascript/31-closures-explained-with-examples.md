# Closures Explained with Examples

A closure is a function that retains access to variables from its enclosing scope even after that outer function has finished executing. This is the mechanism behind private variables, memoization, and factory functions in JavaScript.

```javascript
function makeCounter() {
  let count = 0;
  return () => ++count;
}
const counter = makeCounter();
counter(); // 1
counter(); // 2 - count persisted between calls
```

**Key takeaway:** Every function in JavaScript forms a closure over its surrounding scope - it is not an opt-in feature, it is how scoping fundamentally works.
