# Flexbox Item Properties

Flex children can be tuned individually: flex-grow decides how much extra space an item claims, flex-shrink decides how much it shrinks under pressure, flex-basis sets its starting size, and align-self overrides the container's align-items for just that one item.

```css
.sidebar { flex: 0 0 250px; }  /* do not grow or shrink, fixed 250px */
.main { flex: 1 1 auto; }      /* grow to fill remaining space */
```

**Key takeaway:** flex: 1 is shorthand for flex-grow: 1, flex-shrink: 1, flex-basis: 0% - one of the most-used one-liners in flex layouts.
