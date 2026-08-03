# Conditional Types

A conditional type selects between two types based on a type-level condition, using syntax that mirrors a ternary expression but operates entirely on types rather than values, evaluated by the compiler.

```typescript
type IsString<T> = T extends string ? true : false;
type A = IsString<"hello">; // true
type B = IsString<42>;       // false
```

**Key takeaway:** Conditional types are the mechanism behind many built-in utility types (like Exclude) and enable advanced, reusable type-level logic for library authors.
