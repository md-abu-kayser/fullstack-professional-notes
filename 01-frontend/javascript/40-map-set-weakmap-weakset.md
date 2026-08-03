# Map, Set, WeakMap, WeakSet

Map stores key-value pairs where keys can be any type (unlike plain objects, which coerce keys to strings), and preserves insertion order. Set stores unique values only. WeakMap and WeakSet hold their entries weakly, allowing garbage collection when there are no other references - useful for metadata tied to an object's lifecycle.

```javascript
const cache = new Map();
cache.set({ id: 1 }, "value"); // object keys work directly
const uniqueIds = new Set([1, 2, 2, 3]); // {1, 2, 3}
```

**Key takeaway:** Regular objects silently convert all keys to strings - Map is the correct choice whenever keys need to be objects or need guaranteed order.
