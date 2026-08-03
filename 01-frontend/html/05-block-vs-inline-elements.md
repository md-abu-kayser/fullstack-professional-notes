# Block vs Inline Elements

Block-level elements (like div, p, h1) start on a new line and take up the full width available by default. Inline elements (like span, a, strong) only take up as much width as their content and sit alongside other inline content on the same line. This distinction affects layout before any CSS is even applied.

```html
<div>Block element - starts a new line</div>
<span>Inline element - stays in the flow</span>
```

**Key takeaway:** The CSS display property can override this default behavior entirely.
