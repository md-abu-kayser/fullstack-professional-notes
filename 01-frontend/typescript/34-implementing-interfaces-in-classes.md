# Implementing Interfaces in Classes

A class can declare that it implements one or more interfaces, and the compiler enforces that it provides every member those interfaces require - a useful contract check, though implements is purely compile-time and leaves no runtime trace.

```typescript
interface Serializable {
  toJSON(): string;
}
class User implements Serializable {
  constructor(public name: string) {}
  toJSON() { return JSON.stringify({ name: this.name }); }
}
```

**Key takeaway:** A class can implement multiple interfaces at once, unlike extending only a single base class - useful for composing independent capabilities.
