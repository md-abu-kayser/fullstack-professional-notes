# Optional and Readonly Properties

A question mark after a property name marks it optional, meaning it can be omitted entirely (not just set to undefined). readonly prevents a property from being reassigned after the object is created, though it does not deeply freeze nested objects.

```typescript
interface Config {
  readonly apiKey: string;
  timeout?: number; // optional
}
const config: Config = { apiKey: "abc123" }; // timeout can be omitted
```

**Key takeaway:** readonly is a compile-time-only guarantee - it does not produce a runtime-frozen object like Object.freeze does.
