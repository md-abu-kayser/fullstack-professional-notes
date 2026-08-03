# Utility Type: Partial and Required

Partial<T> makes every property of T optional, commonly used for update or patch functions where only some fields change. Required<T> does the opposite, forcing every optional property to be mandatory.

```typescript
interface User { id: string; name: string; email?: string; }
function updateUser(id: string, changes: Partial<User>) { /* ... */ }
updateUser("1", { name: "New Name" }); // other fields optional
```

**Key takeaway:** Partial is one of the most-used utility types in real codebases, especially for typing PATCH-style update functions cleanly.
