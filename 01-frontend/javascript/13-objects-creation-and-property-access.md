# Objects: Creation and Property Access

Objects can be created with literal syntax, the Object constructor, or Object.create. Properties are accessed with dot notation (fixed key names) or bracket notation (dynamic or non-identifier keys, like ones with spaces or from a variable).

```javascript
const user = { name: "Alex", "favorite-color": "blue" };
const key = "name";
console.log(user[key]);               // dynamic access
console.log(user["favorite-color"]);  // bracket required for hyphenated keys
```

**Key takeaway:** Bracket notation is required whenever the key is dynamic or is not a valid JavaScript identifier.
