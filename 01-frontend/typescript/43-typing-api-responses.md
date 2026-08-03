# Typing API Responses

Defining an interface for an API's response shape and applying it as the generic argument to fetch's .json() call (or via a typed wrapper function) gives compile-time safety for everything consumed from that response, catching typos in property access immediately.

```typescript
interface ApiUser { id: string; name: string; email: string; }

async function getUser(id: string): Promise<ApiUser> {
  const res = await fetch(`/api/users/${id}`);
  return res.json(); // trusted to match ApiUser - see note below
}
```

**Key takeaway:** TypeScript trusts the shape you declare for res.json() - it does not actually validate the response at runtime, so pairing this with a runtime validator like Zod closes that gap.
