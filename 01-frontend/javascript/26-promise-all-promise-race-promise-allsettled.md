# Promise.all, Promise.race, Promise.allSettled

Promise.all runs multiple promises in parallel and resolves once all succeed, but rejects immediately if any one fails. Promise.allSettled waits for all to finish regardless of success or failure, returning the status of each. Promise.race resolves or rejects as soon as the first promise settles, whichever that is.

```javascript
const results = await Promise.allSettled([fetchA(), fetchB(), fetchC()]);
results.forEach(r => console.log(r.status)); // "fulfilled" or "rejected" per item
```

**Key takeaway:** Use allSettled instead of all whenever you need every result, even the failed ones, rather than an all-or-nothing outcome.
