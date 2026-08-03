# Generators and Iterators

A generator function (marked with function*) can pause and resume execution using yield, producing a sequence of values lazily over time instead of all at once. Any object implementing the iterator protocol (a next() method returning {value, done}) can be used in a for-of loop.

```javascript
function* idGenerator() {
  let id = 1;
  while (true) yield id++;
}
const gen = idGenerator();
gen.next().value; // 1
gen.next().value; // 2
```

**Key takeaway:** Generators are the foundation async generators and many streaming/pagination patterns are built on, since they can produce values one at a time on demand.
