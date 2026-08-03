# Nullable Types and the Non-null Assertion

With strictNullChecks enabled, null and undefined must be explicitly included in a type if a value can be one of them. The non-null assertion operator (!) tells the compiler to treat a value as definitely not null or undefined, without an actual runtime check - use it sparingly and only when you are certain.

```typescript
function getElement(id: string): HTMLElement | null {
  return document.getElementById(id);
}
const el = getElement("app")!; // asserting it definitely exists
```

**Key takeaway:** The non-null assertion is a promise, not a guarantee - if the value actually is null at runtime, the resulting error surfaces later and is harder to trace than a proper null check.
