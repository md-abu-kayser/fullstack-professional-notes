# Flexbox vs Grid: When to Use Which

Flexbox excels at one-dimensional layouts - a single row or column of items, like a navbar or a button group. Grid excels at two-dimensional layouts - full page structures with both rows and columns that need to align together, like a dashboard or card gallery.

```css
/* Flexbox: a row of nav links */
nav { display: flex; gap: 16px; }

/* Grid: a full page layout */
body { display: grid; grid-template-columns: 240px 1fr; }
```

**Key takeaway:** In practice, most real layouts use both together - grid for the overall page skeleton, flexbox for smaller components within it.
