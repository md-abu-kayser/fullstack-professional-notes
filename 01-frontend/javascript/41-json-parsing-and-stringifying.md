# JSON: Parsing and Stringifying

JSON.stringify converts a JavaScript value into a JSON-formatted string, commonly used to send data over the network or store it in localStorage. JSON.parse does the reverse, turning a JSON string back into a live JavaScript value. Functions, undefined, and symbols are silently dropped during stringification.

```javascript
const data = { name: "Alex", age: 30, greet: () => {} };
const json = JSON.stringify(data); // {"name":"Alex","age":30} - greet is dropped
const parsed = JSON.parse(json);
```

**Key takeaway:** JSON.stringify silently drops functions and undefined values - never assume a round trip preserves every property of the original object.
