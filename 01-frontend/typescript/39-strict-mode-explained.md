# Strict Mode Explained

strict is actually a shorthand that enables several individual flags together, including noImplicitAny (parameters must have a type or explicit any), strictNullChecks (null and undefined are not assignable to other types by default), and strictFunctionTypes.

```json
{ "compilerOptions": { "strict": true } }
```

```typescript
// With strictNullChecks on:
function greet(name: string | null) {
  console.log(name.toUpperCase()); // Error - name might be null
}
```

**Key takeaway:** strictNullChecks alone catches an enormous share of real-world null/undefined bugs - it is arguably the single highest-value flag in the entire strict bundle.
