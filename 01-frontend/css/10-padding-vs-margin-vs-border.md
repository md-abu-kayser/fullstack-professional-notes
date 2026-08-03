# Padding vs Margin vs Border

Padding is space inside an element's border, between the border and its content - it is part of the element's own background. Margin is space outside the border, separating the element from its neighbors, and is always transparent. Border sits exactly between the two, and can itself be styled with width, color, and style.

```css
.box {
  padding: 16px;        /* inside, has background color */
  border: 1px solid #ccc;
  margin: 24px;          /* outside, always transparent */
}
```

**Key takeaway:** If a background color seems to be "leaking" past an edge you expected, check whether that space is padding (colored) or margin (never colored).
