# Common Next.js Performance Pitfalls

Frequent mistakes include marking components "use client" higher in the tree than necessary (bloating the client bundle), fetching data with cache: "no-store" when it did not need to be dynamic, and importing large libraries into a Client Component instead of keeping them server-side.

```jsx
// Pitfall: entire page marked client just for one button
"use client";
export default function Page() { /* everything here ships to the client */ }
```

**Key takeaway:** Push "use client" down to the smallest possible leaf component - wrapping only the interactive button, not the whole page, keeps the shipped JavaScript minimal.
