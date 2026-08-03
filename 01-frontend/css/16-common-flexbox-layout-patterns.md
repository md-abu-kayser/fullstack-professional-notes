# Common Flexbox Layout Patterns

Flexbox solves everyday layout problems cleanly: centering anything both horizontally and vertically, equal-height columns, a sticky footer that stays at the bottom of a short page, and navbars that space items evenly without manual math.

```css
.center-everything {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 100vh;
}
```

**Key takeaway:** "How do I center a div" has a one-line flexbox answer that replaced years of hacky margin and positioning tricks.
