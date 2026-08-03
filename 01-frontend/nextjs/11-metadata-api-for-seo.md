# Metadata API for SEO

Exporting a static metadata object from a page or layout file lets Next.js generate the corresponding head tags (title, description, Open Graph, etc.) automatically, without manually managing a head element - and metadata merges sensibly down the layout hierarchy.

```jsx
export const metadata = {
  title: "My Blog",
  description: "Thoughts on web development",
};
```

**Key takeaway:** Metadata exported from a layout applies to every nested page unless a more specific page overrides that particular field.
