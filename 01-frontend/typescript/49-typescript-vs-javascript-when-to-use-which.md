# TypeScript vs JavaScript: When to Use Which

TypeScript's compile-time safety pays off most in larger codebases, teams, and long-lived projects where catching errors before runtime and having reliable autocomplete matters. Plain JavaScript can still be reasonable for very small scripts, quick prototypes, or projects with an extremely short lifespan.

```typescript
// The exact same logic, but this version catches type mistakes before running
function calculateTotal(price: number, quantity: number): number {
  return price * quantity;
}
```

**Key takeaway:** Almost every production-scale frontend and backend team today defaults to TypeScript - plain JavaScript is increasingly reserved for scripts, prototypes, or legacy code not yet migrated.
