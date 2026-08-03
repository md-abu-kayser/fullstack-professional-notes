# Generic Constraints

The extends keyword constrains a generic type parameter to only accept types matching a certain shape, letting you safely access properties on a generic value that would otherwise be completely unknown to the compiler.

```typescript
function getLength<T extends { length: number }>(item: T): number {
  return item.length;
}
getLength("hello"); // valid - strings have length
getLength(42);       // Error - numbers do not have length
```

**Key takeaway:** Without a constraint, a bare generic T has no known properties at all - constraints are what let you safely operate on it.
