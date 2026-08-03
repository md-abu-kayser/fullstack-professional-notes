# Const Assertions

Appending as const to a value locks it to its most specific literal type and makes all its properties readonly, which is especially useful for deriving a union type directly from an array or object of allowed values.

```typescript
const roles = ["admin", "editor", "viewer"] as const;
type Role = typeof roles[number]; // "admin" | "editor" | "viewer"
```

**Key takeaway:** as const is the idiomatic way to derive a literal union type from a single array, avoiding having to declare the union and the array separately and keep them in sync.
