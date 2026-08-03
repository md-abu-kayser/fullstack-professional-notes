# Array Destructuring

Destructuring extracts values from an array into individual variables in one line, based on position, with support for skipping elements, default values, and swapping variables without a temporary one.

```javascript
const [first, , third = "default"] = ["a", "b"];
let x = 1, y = 2;
[x, y] = [y, x]; // swap without a temp variable
```

**Key takeaway:** Destructuring makes function returns of multiple values ergonomic - return an array or object and destructure it at the call site.
