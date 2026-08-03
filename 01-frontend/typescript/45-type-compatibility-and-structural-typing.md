# Type Compatibility and Structural Typing

TypeScript uses structural typing ("duck typing") rather than nominal typing - two types are considered compatible if they have the same shape, regardless of their declared names. This differs from languages like Java or C#, where type identity matters more than shape.

```typescript
interface Point { x: number; y: number; }
function logPoint(p: Point) { console.log(p.x, p.y); }
logPoint({ x: 1, y: 2, z: 3 }); // valid - has at least the required shape
```

**Key takeaway:** An object literal passed directly is checked more strictly for excess properties than a variable of a wider type would be - this is called "excess property checking" and can surprise developers coming from nominally-typed languages.
