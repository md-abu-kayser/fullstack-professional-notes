# The as Keyword and Type Assertions

as tells the compiler to treat a value as a specific type without an actual runtime check - useful when you know more about a value's type than TypeScript can infer, but dangerous if used to silence a legitimate type error rather than resolve it.

```typescript
const input = document.getElementById("email") as HTMLInputElement;
console.log(input.value); // value only exists on HTMLInputElement, not Element
```

**Key takeaway:** A type assertion is a promise to the compiler, not a runtime guarantee - if you are wrong, the error surfaces later at runtime instead of at compile time.
