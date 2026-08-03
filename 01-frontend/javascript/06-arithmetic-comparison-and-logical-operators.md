# Arithmetic, Comparison, and Logical Operators

Beyond basic arithmetic (+, -, *, /, %, **), JavaScript has short-circuiting logical operators (&&, ||) and the nullish coalescing operator (??), which only falls back when a value is null or undefined - unlike || which also falls back on 0, "", or false.

```javascript
const count = 0;
console.log(count || 10); // 10 - falsy triggers fallback
console.log(count ?? 10); // 0 - only null/undefined trigger fallback
```

**Key takeaway:** Use ?? instead of || for default values whenever 0, "", or false should be treated as valid, intentional values.
