# Declaration Files (.d.ts)

A .d.ts file contains only type information, no runtime implementation, and is how TypeScript describes the shape of JavaScript code - either your own compiled output, or a third-party library published without built-in types.

```typescript
// math-utils.d.ts
export function add(a: number, b: number): number;
```

**Key takeaway:** Many popular JavaScript libraries ship types separately via the @types/ scope on npm (e.g. @types/lodash) rather than bundling a .d.ts file directly in their own package.
