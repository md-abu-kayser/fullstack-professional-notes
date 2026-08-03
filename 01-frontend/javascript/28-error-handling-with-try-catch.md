# Error Handling with try-catch

try-catch wraps code that might throw, letting you handle failures gracefully instead of crashing the whole script. With async/await, try-catch is the standard way to handle rejected promises, replacing .catch() chains. finally runs regardless of success or failure, useful for cleanup.

```javascript
async function loadData() {
  try {
    const data = await fetchData();
    return data;
  } catch (error) {
    console.error("Failed to load:", error.message);
  } finally {
    hideLoadingSpinner();
  }
}
```

**Key takeaway:** try-catch only catches errors thrown synchronously or from an awaited promise - it will not catch errors from an un-awaited async call inside it.
