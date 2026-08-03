# article vs section vs div

article wraps content that could stand alone and be redistributed independently, like a blog post or news story. section groups related content under a theme, usually with its own heading. div is a generic, non-semantic container used only when no other element fits.

```html
<article>
  <section><h3>Introduction</h3></section>
  <section><h3>Conclusion</h3></section>
</article>
```

**Key takeaway:** If you cannot explain why you chose article or section over div, a div is probably fine.
