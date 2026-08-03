# Function Overloads

Function overloads let a single function name have multiple valid call signatures with different parameter and return types, useful when a function's behavior genuinely varies by input shape in a way a union parameter cannot express cleanly.

```typescript
function getValue(key: string): string;
function getValue(key: string, asNumber: true): number;
function getValue(key: string, asNumber?: boolean): string | number {
  const raw = localStorage.getItem(key) ?? "";
  return asNumber ? Number(raw) : raw;
}
```

**Key takeaway:** Only the overload signatures are visible to callers - the final, combined implementation signature is internal and never directly callable from outside.
