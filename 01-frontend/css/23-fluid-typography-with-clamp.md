# Fluid Typography with clamp

clamp(min, preferred, max) lets a value scale smoothly between a minimum and maximum bound based on the viewport, without needing a media query breakpoint at all. It is most commonly used for font sizes that grow with screen width but never become unreadably small or comically large.

```css
h1 { font-size: clamp(1.5rem, 4vw + 1rem, 3rem); }
```

**Key takeaway:** clamp can replace a whole set of font-size media query breakpoints with a single, smoothly scaling line.
