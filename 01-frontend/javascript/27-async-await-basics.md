# Async-Await Basics

async/await is syntactic sugar over promises that lets asynchronous code read like synchronous code. Any function marked async automatically returns a promise, and await pauses execution within that function (not the whole program) until the awaited promise settles.

```javascript
async function loadUser(id) {
  const user = await fetchUser(id);
  const posts = await fetchPosts(user.id);
  return posts;
}
```

**Key takeaway:** await only pauses the async function it is inside - the rest of the program, including the UI, keeps running normally.
