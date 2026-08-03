# Absolute vs Relative vs Root-Relative URLs

An absolute URL includes the full address including protocol and domain. A relative URL is resolved against the current page's location. A root-relative URL starts from the domain root regardless of current path. Choosing correctly avoids broken links when pages move.

```html
<a href="/blog/post-1">Root-relative</a>
<a href="post-1">Relative to current folder</a>
```

**Key takeaway:** Root-relative links are usually safest for internal navigation in larger sites.
