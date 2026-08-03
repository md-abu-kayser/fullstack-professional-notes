# The Event Loop, Call Stack, and Task Queue

The call stack executes synchronous code one frame at a time. When async work finishes, its callback is placed in a queue rather than run immediately. The event loop's job is simple: once the call stack is completely empty, it pulls the next callback from the queue and pushes it onto the stack to run.

```javascript
console.log("start");
Promise.resolve().then(() => console.log("promise"));
console.log("end");
// Output: start, end, promise
```

**Key takeaway:** The event loop never interrupts running synchronous code - queued callbacks always wait for the call stack to be completely empty first.
