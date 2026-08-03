# Prototypes and Prototypal Inheritance

Every JavaScript object has an internal link to another object called its prototype, forming a chain the engine walks up when a property is not found directly on the object. This prototype chain is how inheritance works under the hood, even for objects created with class syntax.

```javascript
function Animal(name) { this.name = name; }
Animal.prototype.speak = function() { console.log(`${this.name} makes a sound`); };
const dog = new Animal("Rex");
dog.speak(); // found via the prototype chain, not on dog directly
```

**Key takeaway:** class syntax in modern JavaScript is syntactic sugar over this same prototype chain - it did not introduce a new inheritance model.
