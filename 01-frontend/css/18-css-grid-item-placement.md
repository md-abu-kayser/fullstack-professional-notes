# CSS Grid Item Placement

Grid children can be placed explicitly using grid-column and grid-row (with start/end lines), letting an item span multiple tracks regardless of its position in the markup - something flexbox cannot do without reordering the DOM.

```css
.hero { grid-column: 1 / -1; }        /* spans all columns */
.sidebar { grid-row: 2 / 4; }          /* spans rows 2 and 3 */
```

**Key takeaway:** The -1 line always refers to the last grid line, making full-width spans easy without knowing the exact column count.
