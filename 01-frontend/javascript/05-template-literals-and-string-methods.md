# Template Literals and String Methods

Template literals (backtick strings) support embedded expressions with ${} and multi-line strings without concatenation. Combined with common string methods like trim, split, includes, and padStart, they make string handling far more readable than older concatenation-based code.

```javascript
const name = "Alex";
const greeting = `Hello, ${name}!
Welcome back.`;
```

**Key takeaway:** Template literals also support tagged templates - a function can process the literal and its interpolated values before producing the final string.
