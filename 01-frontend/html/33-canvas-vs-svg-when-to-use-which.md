# Canvas vs SVG: When to Use Which

Choose SVG for icons, logos, charts, and anything needing crisp scaling, CSS styling, or accessibility, since each shape stays a real element. Choose canvas for pixel-heavy, high-frequency rendering like games or data visualizations with thousands of points, where DOM overhead would hurt performance.

```html
<!-- SVG: few elements, needs interactivity or styling -->
<!-- Canvas: many elements, needs raw rendering speed -->
```

**Key takeaway:** If you need to reliably click on individual shapes, SVG is almost always the better fit.
