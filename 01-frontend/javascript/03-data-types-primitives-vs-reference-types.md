# Data Types: Primitives vs Reference Types

Primitives (string, number, boolean, null, undefined, symbol, bigint) are immutable and compared by value. Reference types (objects, arrays, functions) are compared by reference, and copying a variable copies the pointer, not the underlying data - a frequent source of "why did my original object change" bugs.

```javascript
let a = { count: 1 };
let b = a;
b.count = 2;
console.log(a.count); // 2 - same object in memory
```

**Key takeaway:** To actually copy an object instead of referencing it, use the spread operator or structuredClone, not simple assignment.
