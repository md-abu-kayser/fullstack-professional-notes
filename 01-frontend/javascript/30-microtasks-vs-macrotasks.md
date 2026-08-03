# Microtasks vs Macrotasks

Promise callbacks and queueMicrotask land in the microtask queue, while setTimeout, setInterval, and I/O callbacks land in the macrotask (or "task") queue. After each single macrotask, the event loop drains the entire microtask queue before rendering or moving to the next macrotask.

```javascript
setTimeout(() => console.log("macrotask"), 0);
Promise.resolve().then(() => console.log("microtask"));
// Output: microtask, then macrotask - microtasks always run first
```

**Key takeaway:** Microtasks always fully drain before the next macrotask runs, which is why a promise callback beats a setTimeout(0) every time.
