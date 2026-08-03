# Common TypeScript Mistakes and Fixes

Frequent mistakes include overusing any to silence errors instead of fixing the underlying type issue, forgetting to narrow a union before accessing type-specific members, and typing a function's return value as any implicitly by not specifying strict mode.

```typescript
// Mistake: silences the error instead of fixing it
function processData(data: any) { return data.value; }

// Fix: define the actual expected shape
function processData(data: { value: string }) { return data.value; }
```

**Key takeaway:** Every any in a codebase is a small hole in type safety - treat each one as a signal to come back and define the real type once it is known.
