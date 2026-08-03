# CSS Transitions

transition animates a property smoothly between its old and new value whenever that value changes - on hover, on class toggle, or on any state change. You specify which property, how long, what easing curve, and an optional delay.

```css
.button {
  background: steelblue;
  transition: background 0.2s ease-in-out;
}
.button:hover { background: navy; }
```

**Key takeaway:** Animating transform and opacity is far cheaper for the browser than animating properties like width or top, which trigger layout recalculation.
