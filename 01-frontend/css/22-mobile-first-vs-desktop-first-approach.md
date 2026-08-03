# Mobile-First vs Desktop-First Approach

Mobile-first means writing base styles for small screens, then using min-width media queries to add complexity as the viewport grows. Desktop-first is the reverse - full styles first, then max-width queries strip things down. Mobile-first tends to produce leaner CSS since simple layouts don't need much overriding.

```css
/* Mobile-first */
.grid { display: block; }
@media (min-width: 900px) {
  .grid { display: grid; grid-template-columns: repeat(3, 1fr); }
}
```

**Key takeaway:** Mobile-first also forces you to prioritize content, since you decide what matters most before you have the luxury of extra screen space.
