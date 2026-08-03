# Type Coercion and Equality: Loose vs Strict

== (loose equality) converts operands to the same type before comparing, which produces surprising results like "" == 0 being true. === (strict equality) compares both type and value with no conversion. Modern style guides and linters recommend always using === unless coercion is explicitly intended.

```javascript
console.log(0 == "0");   // true - coerced
console.log(0 === "0");  // false - different types
```

**Key takeaway:** Default to === everywhere; reserve == only for the rare, well-documented case where coercion is genuinely wanted.
