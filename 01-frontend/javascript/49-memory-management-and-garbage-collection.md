# Memory Management and Garbage Collection

JavaScript automatically allocates and frees memory using garbage collection, primarily via a "mark and sweep" algorithm - objects unreachable from any root reference are eventually cleaned up. Common memory leak causes include forgotten timers, detached DOM references kept in variables, and ever-growing caches with no eviction.

```javascript
// A classic leak: forgetting to clear the interval
const id = setInterval(() => console.log("tick"), 1000);
// clearInterval(id) must eventually be called
```

**Key takeaway:** Holding a reference to a DOM node in a JavaScript variable after removing it from the page prevents that node from ever being garbage collected.
