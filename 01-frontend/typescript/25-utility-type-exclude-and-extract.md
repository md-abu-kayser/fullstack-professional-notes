# Utility Type: Exclude and Extract

Exclude<T, U> removes from union T all members assignable to U. Extract<T, U> does the opposite, keeping only members of T assignable to U - both operate on unions, unlike Omit and Pick which operate on object properties.

```typescript
type Status = "pending" | "active" | "banned" | "deleted";
type ActiveOnly = Exclude<Status, "banned" | "deleted">; // "pending" | "active"
```

**Key takeaway:** Exclude/Extract work on union members; Pick/Omit work on object keys - mixing these two pairs up is a common beginner confusion.
