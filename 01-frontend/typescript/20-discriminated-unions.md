# Discriminated Unions

A discriminated union is a union of object types that all share a common literal property (the "discriminant"), letting TypeScript narrow the entire object's shape based on a single check of that one field - a very common and powerful pattern for representing state.

```typescript
type State =
  | { status: "loading" }
  | { status: "success"; data: string }
  | { status: "error"; message: string };

function render(state: State) {
  if (state.status === "success") console.log(state.data); // safe
}
```

**Key takeaway:** Discriminated unions are the idiomatic TypeScript way to model "one of several possible states," far safer than a single object with many optional fields.
