# Any, Unknown, Never, and Void

any disables type checking entirely for that value - a last resort that should be rare in well-typed code. unknown is a safer alternative that still requires narrowing before use. never represents a value that can never occur (a function that always throws). void represents a function that returns nothing meaningful.

```typescript
function logError(message: string): void { console.error(message); }
function fail(message: string): never { throw new Error(message); }
```

**Key takeaway:** Prefer unknown over any whenever a value's type is genuinely not known yet - it forces you to narrow it before using it, unlike any.
