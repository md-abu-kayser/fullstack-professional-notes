# Caching Strategies in Next.js

Next.js caches at several layers: the fetch cache (memoizing and persisting data requests), the full route cache (statically rendered HTML), and the router cache (client-side navigation cache in the browser). Understanding which layer is stale is often the key to debugging "why isn't my data updating" issues.

```javascript
fetch(url, { cache: "force-cache" });  // default - cache indefinitely
fetch(url, { cache: "no-store" });     // never cache, always fresh
```

**Key takeaway:** "My data is not updating" is almost always a caching layer issue, not a bug - identify which of the three cache layers is serving stale content before changing application code.
