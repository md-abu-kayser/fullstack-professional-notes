# Type Inference vs Explicit Typing

TypeScript can often infer a variable's type from its initial value without an explicit annotation, and this inferred type is just as strictly enforced as one written by hand. Explicit typing becomes necessary mainly for function parameters (which cannot be inferred) and when a variable's type is genuinely ambiguous.

```typescript
let count = 5; // inferred as number, no annotation needed
count = "five"; // Error: Type 'string' is not assignable to type 'number'
```

**Key takeaway:** Over-annotating variables whose type is already obvious from their value just adds noise - let inference do the work where it can.
