# Mapped Types

A mapped type creates a new type by transforming each property of an existing type in a uniform way, using a syntax similar to a for-in loop over the type's keys - this is exactly how utility types like Partial and Readonly are implemented internally.

```typescript
type Optional<T> = { [K in keyof T]?: T[K] };
type ReadonlyVersion<T> = { readonly [K in keyof T]: T[K] };
```

**Key takeaway:** Learning to write your own simple mapped type demystifies how built-in utility types like Partial and Pick actually work under the hood.
