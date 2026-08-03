# Functions: Declarations vs Expressions vs Arrow Functions

Function declarations are hoisted entirely (usable before their definition in code). Function expressions are not hoisted the same way and are often assigned to a variable. Arrow functions have no own this, arguments, or prototype - they inherit this lexically from their enclosing scope.

```javascript
function regular() { console.log(this); }       // dynamic this
const arrow = () => { console.log(this); };      // lexical this
```

**Key takeaway:** Never use an arrow function as an object method if you need this to refer to that object - it will inherit this from the outer scope instead.
