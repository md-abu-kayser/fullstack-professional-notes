# The picture Element and Art Direction

While srcset serves different resolutions of the same crop, picture lets you serve entirely different crops or formats depending on the viewport or browser support - useful when a wide banner needs to become a tighter portrait crop on mobile.

```html
<picture>
  <source media="(max-width: 600px)" srcset="portrait.jpg">
  <img src="landscape.jpg" alt="Mountain view">
</picture>
```

**Key takeaway:** Use picture for art direction with different crops, srcset alone for resolution switching.
