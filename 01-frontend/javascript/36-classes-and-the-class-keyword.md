# Classes and the class Keyword

class syntax provides a cleaner way to write constructor functions and prototype methods, supporting constructor, instance methods, static methods, getters/setters, and inheritance via extends and super - all still built on JavaScript's underlying prototype system.

```javascript
class Animal {
  constructor(name) { this.name = name; }
  speak() { console.log(`${this.name} makes a sound`); }
}
class Dog extends Animal {
  speak() { super.speak(); console.log(`${this.name} barks`); }
}
```

**Key takeaway:** Class methods are non-enumerable and added to the prototype automatically, unlike properties assigned directly in the constructor.
