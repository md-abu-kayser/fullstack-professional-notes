# Loops: for, while, do-while

for is ideal when the number of iterations is known in advance. while checks its condition before each iteration and may never run. do-while checks after each iteration, guaranteeing the body runs at least once - useful for retry logic or input validation loops.

```javascript
let attempts = 0;
do {
  attempts++;
} while (attempts < 3);
```

**Key takeaway:** Prefer array methods (map, forEach, filter) over manual for loops when working with arrays - they are more declarative and less error-prone.
