# Truthy and Falsy Values

Every value in JavaScript is truthy except a specific short list of falsy values: false, 0, -0, "", null, undefined, and NaN. Everything else, including "0" (a non-empty string), [] (an empty array), and {} (an empty object), is truthy.

```javascript
if ([]) console.log("arrays are truthy, even empty ones");
if ("0") console.log("non-empty strings are truthy, even '0'");
```

**Key takeaway:** An empty array or object is truthy - a very common source of bugs when checking "is this list empty" with a plain if statement instead of checking .length.
