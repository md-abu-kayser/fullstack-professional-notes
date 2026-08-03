# Inline vs Internal vs External CSS

There are three ways to apply CSS: inline (a style attribute directly on an element), internal (a style tag inside the document head), and external (a separate .css file linked via link). External stylesheets are the standard for real projects since they are cacheable across pages, reusable, and keep markup clean and readable.

```html
<link rel="stylesheet" href="styles.css">
<style> p { color: green; } </style>
<p style="color: red;">Inline wins here</p>
```

**Key takeaway:** Inline styles have the highest specificity of the three, which is exactly why professional teams use them sparingly - usually only for dynamic, JS-driven values.
