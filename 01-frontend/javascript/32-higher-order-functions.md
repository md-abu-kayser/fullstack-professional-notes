# Higher-Order Functions

A higher-order function either accepts a function as an argument, returns a function, or both. map, filter, and reduce are all higher-order functions built into arrays, and custom ones let you compose reusable, flexible logic instead of duplicating similar code.

```javascript
function withLogging(fn) {
  return (...args) => {
    console.log("Calling with:", args);
    return fn(...args);
  };
}
const loggedAdd = withLogging((a, b) => a + b);
```

**Key takeaway:** Treating functions as regular values you can pass around is the foundation of functional programming patterns in JavaScript.
