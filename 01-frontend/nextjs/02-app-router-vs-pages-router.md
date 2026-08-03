# App Router vs Pages Router

The Pages Router (the original system, files under pages/) maps one file to one route with simple, file-based conventions. The App Router (files under app/) is the modern default, built on React Server Components, supporting nested layouts, streaming, and colocated loading/error states that the Pages Router cannot express natively.

```
app/
  layout.tsx
  page.tsx
  about/
    page.tsx
```

**Key takeaway:** New projects should default to the App Router - the Pages Router still works but is in maintenance mode for new feature development.
