# Callbacks and Callback Hell

A callback is simply a function passed into another function to be called later, often when an async operation completes. Nesting many callbacks inside each other for sequential async steps creates "callback hell" - deeply indented, hard-to-follow code that promises and async/await were designed to solve.

```javascript
getUser(id, (user) => {
  getPosts(user.id, (posts) => {
    getComments(posts[0].id, (comments) => {
      console.log(comments); // deeply nested - hard to read and debug
    });
  });
});
```

**Key takeaway:** Callback hell is a structural problem, not a callback problem - the same logic written with async/await reads top to bottom instead of triangle-shaped.
