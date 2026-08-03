# Decorators Overview

Decorators are functions that can annotate and modify classes, methods, or properties at definition time, commonly used in frameworks like Angular and NestJS for things like dependency injection metadata or route registration. They require enabling a compiler flag and are still stabilizing as a language feature.

```typescript
function Log(target: any, propertyKey: string, descriptor: PropertyDescriptor) {
  const original = descriptor.value;
  descriptor.value = function (...args: any[]) {
    console.log(`Calling ${propertyKey}`);
    return original.apply(this, args);
  };
}
```

**Key takeaway:** Decorators are mostly encountered through a framework's conventions (like NestJS's @Controller) rather than written from scratch in typical application code.
