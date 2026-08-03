# SVG Basics and Inline SVG

SVG describes images with XML-based shapes rather than pixels, so it scales to any size without blurring. Written inline in HTML, each shape becomes a real DOM node that can be styled with CSS and manipulated with JavaScript, unlike canvas.

```html
<svg viewBox="0 0 100 100" width="100" height="100">
  <circle cx="50" cy="50" r="40" fill="steelblue"/>
</svg>
```

**Key takeaway:** Inline SVG shapes can be targeted and animated with plain CSS selectors, just like any other element.
