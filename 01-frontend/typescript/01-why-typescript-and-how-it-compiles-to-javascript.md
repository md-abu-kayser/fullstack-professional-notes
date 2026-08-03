# Why TypeScript and How It Compiles to JavaScript

TypeScript is a superset of JavaScript that adds static typing, checked at compile time rather than discovered at runtime. The TypeScript compiler (tsc) strips all type annotations and emits plain JavaScript - types exist purely as a development-time safety net and leave zero trace in the shipped code.

```typescript
function add(a: number, b: number): number {
  return a + b;
}
// Compiles to plain JS with no type annotations at all
```

**Key takeaway:** Types have zero runtime cost - they cannot be checked or inspected in production code, only during compilation.
