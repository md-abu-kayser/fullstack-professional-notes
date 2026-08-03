# Type Aliases vs Interfaces

For plain object shapes, the two are largely interchangeable. Interfaces support declaration merging and are generally preferred for public API shapes and class contracts. Type aliases are required for unions, intersections, tuples, and mapped types, which interfaces cannot express directly.

```typescript
type ID = string | number;       // must be a type alias - interfaces cannot do unions
interface Point { x: number; y: number; } // idiomatic for object shapes
```

**Key takeaway:** A common team convention is: interfaces for object/class shapes, type aliases for everything else (unions, tuples, function types).
