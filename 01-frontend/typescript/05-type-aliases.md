# Type Aliases

A type alias gives a name to any type - a primitive, a union, an object shape, or a function signature - improving readability and letting you reuse a complex type definition across a codebase without repeating it.

```typescript
type UserId = string;
type Status = "pending" | "active" | "banned";
type User = { id: UserId; status: Status };
```

**Key takeaway:** Unlike interfaces, type aliases can represent unions, primitives, and tuples directly - not just object shapes.
