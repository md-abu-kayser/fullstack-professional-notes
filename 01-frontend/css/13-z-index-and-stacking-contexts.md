# Z-index and Stacking Contexts

z-index controls which element sits on top when boxes overlap, but only works on positioned elements (anything other than static). Higher values sit on top of lower ones. Certain CSS properties (like opacity < 1, transform, or filter) create a new stacking context, which can trap z-index values inside it regardless of how high they are set.

```css
.modal { position: fixed; z-index: 1000; }
.overlay { position: fixed; z-index: 999; }
```

**Key takeaway:** If a high z-index still is not working, check whether a parent element accidentally created its own stacking context via transform or opacity.
