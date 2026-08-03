# CSS Grid vs Flexbox for Card Layouts

A row of equal-width cards that should wrap can be built with either, but grid handles the wrapping and equal sizing more predictably via auto-fit/auto-fill and minmax(), without needing explicit width calculations on each card.

```css
.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 16px;
}
```

**Key takeaway:** auto-fit with minmax() is the single most useful one-liner for a responsive card grid with zero media queries.
