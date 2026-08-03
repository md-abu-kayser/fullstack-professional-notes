# Synchronous vs Asynchronous Code

Synchronous code executes line by line, each statement blocking the next until it finishes. Asynchronous code lets long-running operations (network requests, timers, file I/O) run in the background without blocking the main thread, with results delivered later via callbacks, promises, or async/await.

```javascript
console.log("1");
setTimeout(() => console.log("2"), 0);
console.log("3");
// Output: 1, 3, 2 - the timeout callback runs after the synchronous code finishes
```

**Key takeaway:** Even a setTimeout of 0ms is deferred until after all currently queued synchronous code finishes running.
