# Incremental Static Regeneration

ISR lets a statically generated page be automatically regenerated in the background after a specified time interval, combining the speed of static pages with data that is periodically refreshed - visitors get the fast cached version while a new one builds behind the scenes.

```jsx
const res = await fetch("https://api.example.com/posts", {
  next: { revalidate: 60 }, // regenerate at most once every 60 seconds
});
```

**Key takeaway:** ISR serves the previously cached page instantly while regenerating in the background - no visitor ever waits for the rebuild to happen.
