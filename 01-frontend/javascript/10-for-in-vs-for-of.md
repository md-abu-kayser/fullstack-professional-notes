# for-in vs for-of

for-in iterates over the enumerable property keys of an object (including inherited ones, without care), which makes it a poor fit for arrays. for-of iterates over the values of any iterable (arrays, strings, Maps, Sets), which is almost always what you actually want for array iteration.

```javascript
const arr = ["a", "b", "c"];
for (const value of arr) console.log(value); // "a", "b", "c"
for (const key in arr) console.log(key);      // "0", "1", "2" (strings!)
```

**Key takeaway:** Never use for-in on arrays - it iterates keys as strings and can pick up inherited enumerable properties unexpectedly.
