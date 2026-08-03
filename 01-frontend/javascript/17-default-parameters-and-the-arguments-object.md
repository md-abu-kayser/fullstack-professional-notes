# Default Parameters and the Arguments Object

Default parameters let a function fall back to a specified value when an argument is undefined or omitted. The older arguments object gives access to all passed arguments in regular functions (not arrow functions) but is largely superseded by rest parameters, which produce a real array.

```javascript
function greet(name = "Guest") {
  console.log(`Hello, ${name}`);
}
```

**Key takeaway:** arguments does not exist inside arrow functions at all - use rest parameters there instead.
