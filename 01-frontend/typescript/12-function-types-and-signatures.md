# Function Types and Signatures

A function's type describes its parameter types and return type, and can be written inline or extracted into a reusable type alias - useful for typing callback parameters, event handlers, or higher-order functions consistently.

```typescript
type MathOperation = (a: number, b: number) => number;
const add: MathOperation = (a, b) => a + b;
const subtract: MathOperation = (a, b) => a - b;
```

**Key takeaway:** Extracting a function type alias once and reusing it across multiple implementations keeps signatures consistent and easy to change in one place.
