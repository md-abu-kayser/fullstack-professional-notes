# Flexbox Container Properties

Flexbox is a one-dimensional layout model controlled from the parent (display: flex). Key container properties: flex-direction (row or column), justify-content (alignment along the main axis), align-items (alignment along the cross axis), and flex-wrap (whether items wrap to new lines).

```css
.container {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
}
```

**Key takeaway:** justify-content works on the main axis and align-items on the cross axis - swap flex-direction to column and their effects visually swap too.
