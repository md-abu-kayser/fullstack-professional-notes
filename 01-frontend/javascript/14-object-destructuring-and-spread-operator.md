# Object Destructuring and Spread Operator

Object destructuring pulls named properties out into variables, with support for renaming and defaults. The spread operator (...) shallow-copies an object's own enumerable properties into a new object, commonly used for immutable updates.

```javascript
const { name: userName = "Guest", age } = user;
const updatedUser = { ...user, age: age + 1 };
```

**Key takeaway:** Spread only performs a shallow copy - nested objects inside are still shared by reference with the original.
