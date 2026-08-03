# Array Methods: map, filter, reduce

map transforms each element and returns a new array of the same length. filter returns a new array containing only elements that pass a test. reduce folds the entire array down into a single accumulated value - a sum, an object, or anything else.

```javascript
const nums = [1, 2, 3, 4];
const doubled = nums.map(n => n * 2);
const evens = nums.filter(n => n % 2 === 0);
const total = nums.reduce((sum, n) => sum + n, 0);
```

**Key takeaway:** All three are non-mutating - they return new arrays or values, leaving the original array untouched.
