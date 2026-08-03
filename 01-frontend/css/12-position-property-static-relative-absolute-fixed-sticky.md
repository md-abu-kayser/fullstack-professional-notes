# Position Property: static, relative, absolute, fixed, sticky

static is the default - no special positioning. relative shifts an element from its normal position without affecting layout flow. absolute removes it from flow entirely, positioning it relative to its nearest positioned ancestor. fixed positions relative to the viewport and stays put on scroll. sticky toggles between relative and fixed based on scroll position.

```css
.parent { position: relative; }
.badge { position: absolute; top: 0; right: 0; }
.navbar { position: sticky; top: 0; }
```

**Key takeaway:** absolute only positions relative to the nearest ancestor that has any position other than static - a very common source of "why is this in the wrong place" bugs.
