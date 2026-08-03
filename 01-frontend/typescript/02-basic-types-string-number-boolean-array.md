# Basic Types: string, number, boolean, array

The core primitive types mirror JavaScript's: string, number, and boolean. Arrays are typed with a suffix (number[]) or generic syntax (Array<number>), and tuples describe a fixed-length array with specific types per position.

```typescript
let name: string = "Alex";
let scores: number[] = [90, 85, 78];
let point: [number, number] = [10, 20]; // tuple
```

**Key takeaway:** A tuple enforces both length and per-position type - assigning a third element to a two-element tuple is a compile error.
