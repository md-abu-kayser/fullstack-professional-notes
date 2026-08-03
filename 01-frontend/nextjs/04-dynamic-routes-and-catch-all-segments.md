# Dynamic Routes and Catch-all Segments

Square-bracket folder names create dynamic route segments, whose value is available as a parameter inside the page. Adding an ellipsis inside the brackets creates a catch-all segment that matches multiple path parts, and a double-bracket variant makes that catch-all optional.

```
app/blog/[slug]/page.tsx        -> /blog/my-post (params.slug = "my-post")
app/docs/[...slug]/page.tsx     -> /docs/a/b/c (params.slug = ["a","b","c"])
```

**Key takeaway:** Optional catch-all segments ([[...slug]]) also match the base route itself, which regular catch-all segments do not.
