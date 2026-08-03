# Promises: States and Chaining

A promise represents a value that may not be available yet, existing in one of three states: pending, fulfilled, or rejected. .then() chains additional steps after fulfillment, .catch() handles rejection, and each .then() returns a new promise, enabling clean sequential chains instead of nested callbacks.

```javascript
fetchUser(id)
  .then(user => fetchPosts(user.id))
  .then(posts => console.log(posts))
  .catch(error => console.error(error));
```

**Key takeaway:** A promise settles exactly once - it cannot go from fulfilled back to pending, or resolve twice with different values.
