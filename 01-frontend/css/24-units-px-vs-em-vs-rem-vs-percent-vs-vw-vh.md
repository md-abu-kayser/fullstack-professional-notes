# Units: px vs em vs rem vs percent vs vw-vh

px is an absolute unit, fixed regardless of context. em is relative to the font-size of the parent element (compounding when nested). rem is relative to the root html element's font-size only (no compounding, more predictable). Percentages are relative to the parent's corresponding dimension. vw/vh are relative to 1% of the viewport width/height.

```css
html { font-size: 16px; }
.card { padding: 1rem; }   /* always 16px, regardless of nesting */
.text { font-size: 1.2em; } /* relative to its own parent's font-size */
```

**Key takeaway:** Prefer rem for font sizes and spacing in real projects - it avoids the compounding surprises em can cause in deeply nested components.
