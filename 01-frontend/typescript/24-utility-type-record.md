# Utility Type: Record

Record<Keys, Type> constructs an object type with a specific set of keys, all mapped to the same value type - a concise way to type lookup objects, dictionaries, and maps keyed by a known literal union.

```typescript
type Role = "admin" | "editor" | "viewer";
const permissions: Record<Role, string[]> = {
  admin: ["read", "write", "delete"],
  editor: ["read", "write"],
  viewer: ["read"],
};
```

**Key takeaway:** Using Record with a literal union as the key also forces you to provide a value for every possible key - omitting one is a compile error.
