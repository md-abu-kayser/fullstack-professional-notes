# call, apply, and bind

All three explicitly control what this refers to inside a function. call invokes the function immediately with arguments listed individually. apply invokes it immediately with arguments as an array. bind does not invoke immediately - it returns a new function with this permanently locked in, callable later.

```javascript
function greet(greeting) { console.log(`${greeting}, ${this.name}`); }
greet.call({ name: "Alex" }, "Hi");
const boundGreet = greet.bind({ name: "Sam" });
boundGreet("Hello");
```

**Key takeaway:** bind is especially useful for event handlers in class components, where a method's this would otherwise be lost when passed as a callback.
