# Index Signatures

An index signature describes the type of properties on an object when the exact key names are not known in advance, only their general type - useful for describing dictionary-like objects with dynamic keys.

```typescript
interface StringDictionary {
  [key: string]: string;
}
const translations: StringDictionary = { hello: "hola", bye: "adiós" };
```

**Key takeaway:** Prefer Record<string, T> over a hand-written index signature for simple dictionary shapes - it reads more clearly and is the idiomatic modern choice.
