# Rest Parameters vs Spread Operator

They use the same ... syntax but do opposite jobs depending on context. Rest parameters collect multiple arguments into a single array inside a function signature. Spread expands an array or object out into individual elements or properties.

```javascript
function sum(...numbers) { // rest: gathers args into an array
  return numbers.reduce((a, b) => a + b, 0);
}
sum(...[1, 2, 3]); // spread: expands the array into arguments
```

**Key takeaway:** Rest gathers, spread expands - the direction of ... depends entirely on where it appears.
