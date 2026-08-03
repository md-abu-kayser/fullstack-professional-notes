# Common TypeScript Interview Questions and Answers

Frequent topics include: explaining the difference between interface and type, what structural typing means compared to nominal typing, how generics improve on any, and when you would use unknown instead of any.

```typescript
// A common live-coding prompt: write a generic function
function firstItem<T>(arr: T[]): T | undefined {
  return arr[0];
}
```

**Key takeaway:** Interviewers often want to see you reach for a generic instead of any when a function's behavior should adapt to whatever type is passed in.
