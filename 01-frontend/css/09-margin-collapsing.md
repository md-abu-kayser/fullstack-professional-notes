# Margin Collapsing

When two vertical margins meet - like the bottom margin of one element and the top margin of the next sibling - they do not add together. Instead, the browser collapses them into a single margin equal to the larger of the two. This only happens vertically, and only under specific conditions (not with flex or grid children).

```css
p { margin-bottom: 20px; }
h2 { margin-top: 30px; }
/* Gap between them is 30px, not 50px */
```

**Key takeaway:** Margin collapsing does not happen inside flex or grid containers, which is one reason many teams reach for those layouts to get predictable spacing.
