# Type Narrowing with typeof and instanceof

TypeScript automatically narrows a union type within a conditional block based on runtime checks like typeof (for primitives) or instanceof (for class instances), letting you safely access type-specific members inside that branch.

```typescript
function format(value: string | Date) {
  if (value instanceof Date) {
    return value.toISOString(); // narrowed to Date here
  }
  return value.trim(); // narrowed to string here
}
```

**Key takeaway:** Narrowing is purely a compile-time analysis of your runtime checks - TypeScript is smart enough to follow standard JavaScript conditionals without any special syntax.
