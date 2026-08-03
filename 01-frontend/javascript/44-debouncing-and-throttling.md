# Debouncing and Throttling

Debouncing delays running a function until a burst of calls has stopped for a specified time, ideal for search-as-you-type inputs. Throttling ensures a function runs at most once per specified interval regardless of how often it is triggered, ideal for scroll or resize handlers.

```javascript
function debounce(fn, delay) {
  let timer;
  return (...args) => {
    clearTimeout(timer);
    timer = setTimeout(() => fn(...args), delay);
  };
}
```

**Key takeaway:** Debounce answers "wait until the user stops"; throttle answers "no more than once every X ms" - they solve different problems and are not interchangeable.
