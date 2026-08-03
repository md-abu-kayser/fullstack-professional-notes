# Type Guards and Custom Type Predicates

Beyond built-in narrowing (typeof, instanceof), you can write a custom function whose return type is a type predicate (value is SomeType), teaching the compiler to narrow a value's type based on that function's boolean result.

```typescript
interface Cat { meow(): void; }
interface Dog { bark(): void; }

function isCat(animal: Cat | Dog): animal is Cat {
  return "meow" in animal;
}
```

**Key takeaway:** A custom type guard is essential whenever narrowing logic is too complex for a single typeof or instanceof check to express directly.
