# CSS Grid Container Properties

CSS Grid is a two-dimensional layout system controlled from the parent (display: grid). grid-template-columns and grid-template-rows define the track sizes, gap adds spacing between cells without margin hacks, and grid-template-areas lets you name regions for very readable layouts.

```css
.layout {
  display: grid;
  grid-template-columns: 250px 1fr;
  grid-template-rows: auto 1fr auto;
  gap: 16px;
}
```

**Key takeaway:** Grid handles rows and columns simultaneously - reach for it over flexbox whenever a layout needs alignment in both directions at once.
