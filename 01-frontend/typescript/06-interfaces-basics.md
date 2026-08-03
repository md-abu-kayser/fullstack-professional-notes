# Interfaces Basics

An interface describes the shape an object must conform to - its property names and their types. Interfaces are the conventional choice for defining object and class shapes in TypeScript, supporting extension via extends for building up related shapes.

```typescript
interface User {
  id: string;
  name: string;
  email: string;
}

interface Admin extends User {
  permissions: string[];
}
```

**Key takeaway:** Interfaces with the same name in the same scope automatically merge their members - a feature called declaration merging that type aliases do not have.
