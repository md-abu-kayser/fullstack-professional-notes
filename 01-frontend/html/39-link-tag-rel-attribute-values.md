# Link Tag: rel Attribute Values

link connects external resources to the document, most commonly stylesheets, but the rel attribute unlocks many other uses: preload hints the browser to fetch a critical resource early, canonical tells search engines the authoritative URL for duplicate content, and icon sets the favicon.

```html
<link rel="stylesheet" href="styles.css">
<link rel="canonical" href="https://example.com/original-page">
```

**Key takeaway:** rel="canonical" is essential whenever the same content is reachable through multiple URLs.
