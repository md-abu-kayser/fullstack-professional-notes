# Symbols and Their Use Cases

A symbol is a unique, immutable primitive value, guaranteed never to collide with another symbol even if created with the same description. They are commonly used as non-string object keys to avoid property name collisions, and to implement well-known protocols like Symbol.iterator.

```javascript
const id = Symbol("id");
const user = { [id]: 123, name: "Alex" };
// user[id] cannot collide with any string-keyed property
```

**Key takeaway:** Symbol-keyed properties are skipped by JSON.stringify, for-in, and Object.keys - they are effectively hidden from typical enumeration.
