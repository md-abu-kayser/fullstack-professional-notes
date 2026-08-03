# Loading and Error UI Conventions

A loading.tsx file in a route folder automatically wraps that segment in a Suspense boundary, showing instantly while the page's data fetch is in flight. An error.tsx file automatically wraps the segment in an error boundary, catching rendering errors in that segment without crashing the whole app.

```jsx
// app/dashboard/loading.tsx
export default function Loading() {
  return <Spinner />;
}
```

**Key takeaway:** These are pure file-naming conventions - no manual Suspense or error boundary wiring is required, Next.js wires them up automatically based on file presence.
