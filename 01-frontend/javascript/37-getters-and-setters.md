# Getters and Setters

get and set define methods that behave like regular properties from the outside, letting you run logic (validation, computed values, logging) transparently whenever a property is read or assigned, without changing how consumers of the object interact with it.

```javascript
class Temperature {
  #celsius = 0;
  get fahrenheit() { return this.#celsius * 9 / 5 + 32; }
  set fahrenheit(value) { this.#celsius = (value - 32) * 5 / 9; }
}
```

**Key takeaway:** Getters and setters let you change internal representation later without breaking any code that reads or writes the public property.
