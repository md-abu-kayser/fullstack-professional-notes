# var vs let vs const

var is function-scoped and hoisted with an initial value of undefined, which causes confusing bugs in loops and conditionals. let is block-scoped and hoisted but not initialized (the "temporal dead zone"). const is block-scoped like let but cannot be reassigned - though objects and arrays declared with const can still have their contents mutated.

```javascript
const user = { name: "Alex" };
user.name = "Sam"; // valid - the object is mutated, not reassigned
// user = {} would throw a TypeError
```

**Key takeaway:** const prevents reassignment, not mutation - reach for Object.freeze if you need true immutability.
