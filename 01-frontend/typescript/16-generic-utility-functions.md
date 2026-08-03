# Generic Utility Functions

Generic functions are especially valuable for reusable utilities - a typed wrapper around fetch, a generic array-grouping helper, or a generic state container - where the exact data shape varies by call site but the logic stays identical.

```typescript
function groupBy<T, K extends string | number>(items: T[], keyFn: (item: T) => K) {
  return items.reduce((acc, item) => {
    const key = keyFn(item);
    (acc[key] ??= []).push(item);
    return acc;
  }, {} as Record<K, T[]>);
}
```

**Key takeaway:** Writing a utility generically once, rather than duplicating it per data type, is one of the clearest practical payoffs of learning generics well.
