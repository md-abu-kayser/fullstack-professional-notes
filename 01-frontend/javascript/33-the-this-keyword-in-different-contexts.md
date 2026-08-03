# The this Keyword in Different Contexts

this refers to different things depending on how a function is called, not where it is defined (except for arrow functions). As a plain function call, this is undefined in strict mode. As a method call (obj.method()), this is the object before the dot. In an arrow function, this is inherited lexically from the enclosing scope.

```javascript
const obj = {
  name: "Alex",
  regular() { console.log(this.name); }, // "Alex" - called as obj.regular()
  arrow: () => console.log(this.name),    // undefined - lexical this
};
```

**Key takeaway:** this is determined by how a function is called, not where it is written - except for arrow functions, which ignore call-site entirely.
