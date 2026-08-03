# Common JavaScript Interview Questions and Answers

Frequent topics include: explaining closures with a concrete example, the difference between == and ===, how the event loop and microtask queue work, what "this" refers to in various contexts, and the practical difference between var, let, and const in loops.

```javascript
// Classic "var in a loop" gotcha
for (var i = 0; i < 3; i++) {
  setTimeout(() => console.log(i), 0); // logs 3, 3, 3 - var is function-scoped
}
```

**Key takeaway:** Interviewers often use the "var in a setTimeout loop" example specifically to test whether you understand scoping, not just syntax.
