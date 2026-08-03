# Generics Basics

Generics let a function, interface, or class work with a variety of types while preserving the specific type used at each call site, rather than falling back to any and losing type safety entirely.

```typescript
function identity<T>(value: T): T {
  return value;
}
const num = identity(42);      // T inferred as number
const str = identity("hello"); // T inferred as string
```

**Key takeaway:** Generics preserve the actual input type in the return type - unlike any, the caller still gets full type safety and autocomplete on the result.
