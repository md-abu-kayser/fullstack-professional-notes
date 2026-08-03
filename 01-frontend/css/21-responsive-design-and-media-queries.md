# Responsive Design and Media Queries

Media queries apply CSS conditionally based on characteristics of the viewport, most commonly its width. They are the foundation of responsive design, letting a single stylesheet adapt a layout across phones, tablets, and desktops.

```css
.container { padding: 16px; }

@media (min-width: 768px) {
  .container { padding: 32px; }
}
```

**Key takeaway:** Combine media queries with a mobile-first approach (min-width queries building up) rather than max-width queries building down - it usually produces cleaner CSS.
