# Utility Type: ReturnType and Parameters

ReturnType<F> extracts the return type of a function type without repeating it manually. Parameters<F> extracts a tuple of its parameter types. Both are especially useful for deriving types from third-party or generated functions whose signatures you do not own.

```typescript
function createUser(name: string, age: number) {
  return { id: crypto.randomUUID(), name, age };
}
type NewUser = ReturnType<typeof createUser>;
```

**Key takeaway:** ReturnType<typeof fn> is the standard pattern for deriving a type from an existing function's return value instead of manually duplicating its shape.
