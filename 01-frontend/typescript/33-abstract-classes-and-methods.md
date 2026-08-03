# Abstract Classes and Methods

An abstract class cannot be instantiated directly - it exists only to be extended, and can declare abstract methods that have no implementation, forcing every subclass to provide one. This is useful for enforcing a shared contract across a family of related classes.

```typescript
abstract class Shape {
  abstract area(): number;
  describe() { return `Area: ${this.area()}`; }
}
class Circle extends Shape {
  constructor(private radius: number) { super(); }
  area() { return Math.PI * this.radius ** 2; }
}
```

**Key takeaway:** Unlike an interface, an abstract class can provide real, shared implementation (like describe above) alongside the methods it forces subclasses to implement.
