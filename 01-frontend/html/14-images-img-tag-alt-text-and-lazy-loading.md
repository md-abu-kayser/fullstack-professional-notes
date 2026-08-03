# Images: img Tag, alt Text, and Lazy Loading

The img tag embeds images via its src attribute. The alt attribute is not optional in practice - it describes the image for screen readers and displays if the image fails to load. The loading="lazy" attribute defers off-screen images until the user scrolls near them, improving initial page load.

```html
<img src="hero.jpg" alt="Team celebrating a product launch" loading="lazy">
```

**Key takeaway:** Decorative images should use an empty alt (not omitted) so screen readers skip them.
