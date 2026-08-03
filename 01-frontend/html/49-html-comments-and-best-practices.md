# HTML Comments and Best Practices

HTML comments are invisible to visitors but visible in page source, so they should never contain sensitive information like internal notes, TODOs with security implications, or commented-out credentials. They are useful for marking sections in long templates or leaving brief context for other developers.

```html
<!-- Header section starts here -->
<header>...</header>
```

**Key takeaway:** Anything inside an HTML comment is still downloaded by every visitor - never hide secrets there.
