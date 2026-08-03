# Working with Untyped Third-Party Libraries

When a library has no bundled types and no @types/ package available, you can write a minimal ambient declaration file describing just enough of its shape to use it safely, or fall back to declaring it as any with a clear comment explaining why.

```typescript
// legacy-lib.d.ts
declare module "legacy-lib" {
  export function doSomething(input: string): void;
}
```

**Key takeaway:** A minimal hand-written declaration file is almost always better than sprinkling as any throughout your own application code every time you use the library.
