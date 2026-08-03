# Introduction to JavaScript and How It Runs

JavaScript is a single-threaded, interpreted (JIT-compiled in practice) language that runs in browsers and, via Node.js, on servers. Its engine (V8 in Chrome and Node) parses code, compiles it just-in-time, and executes it on one main thread - asynchronous behavior is handled through the event loop, not real parallel threads.

```javascript
console.log("Hello, World!");
```

**Key takeaway:** JavaScript being single-threaded is exactly why blocking operations (huge loops, synchronous file reads) freeze the whole page or server until they finish.

**Interview angle:** Be ready to explain that "single-threaded" does not mean "cannot do async work" - the event loop is the mechanism that reconciles the two.
