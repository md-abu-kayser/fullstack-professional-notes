# Literal Types

A literal type restricts a value to one exact, specific value rather than a general type like string. Combined with unions, literal types create precise, enum-like sets of allowed values that autocomplete and catch typos at compile time.

```typescript
type Direction = "north" | "south" | "east" | "west";
function move(direction: Direction) { /* ... */ }
move("north");  // valid
move("up");     // Error: not assignable to type 'Direction'
```

**Key takeaway:** String literal unions are often a lighter-weight, more ergonomic alternative to enums for a fixed set of string values.
