# Never Type in Exhaustive Checks

Assigning a value to a variable typed never inside the default case of a switch over a union causes a compile error if any union member was left unhandled - a powerful pattern for ensuring that adding a new variant to a union is caught everywhere it needs to be handled.

```typescript
type Shape = { kind: "circle" } | { kind: "square" };

function area(shape: Shape) {
  switch (shape.kind) {
    case "circle": return 1;
    case "square": return 2;
    default:
      const _exhaustive: never = shape; // errors if a case was missed
      return _exhaustive;
  }
}
```

**Key takeaway:** This exhaustiveness check pattern turns "I added a new union member but forgot to handle it somewhere" into an immediate compile error instead of a silent runtime bug.
