# Union Types

A union type (A | B) means a value can be one of several specified types. TypeScript requires narrowing a union before you can safely use type-specific members, since only properties common to all members of the union are accessible without a check.

```typescript
function printId(id: string | number) {
  if (typeof id === "string") {
    console.log(id.toUpperCase()); // safe - narrowed to string here
  }
}
```

**Key takeaway:** Accessing a property that only exists on one branch of a union without narrowing first is a compile error, by design.
