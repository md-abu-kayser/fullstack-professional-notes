# Utility Type: Pick and Omit

Pick<T, Keys> constructs a new type containing only the specified properties from T. Omit<T, Keys> does the reverse, constructing a new type with everything except the specified properties - both avoid manually redeclaring a near-duplicate interface.

```typescript
interface User { id: string; name: string; password: string; }
type PublicUser = Omit<User, "password">;
type UserPreview = Pick<User, "id" | "name">;
```

**Key takeaway:** Omit<User, "password"> is a common, safe pattern for defining exactly what shape is safe to send to the client, derived from a single source of truth.
