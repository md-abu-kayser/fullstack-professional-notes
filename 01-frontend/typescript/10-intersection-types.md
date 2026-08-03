# Intersection Types

An intersection type (A & B) combines multiple types into one that must satisfy all of them simultaneously - useful for composing smaller, reusable shapes into a larger one without repeating properties.

```typescript
type Timestamped = { createdAt: Date };
type Named = { name: string };
type Entity = Timestamped & Named; // must have both createdAt and name
```

**Key takeaway:** Where unions mean "one of these," intersections mean "all of these at once" - opposite operations that are easy to mix up when first learning TypeScript.
