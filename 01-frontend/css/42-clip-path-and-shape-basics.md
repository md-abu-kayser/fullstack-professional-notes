# Clip-path and Shape Basics

clip-path defines a visible region for an element, hiding everything outside it - useful for custom shapes like hexagons, diagonal banner cuts, or circular avatars, without needing extra markup or image masks.

```css
.avatar { clip-path: circle(50%); }
.banner { clip-path: polygon(0 0, 100% 0, 100% 80%, 0 100%); }
```

**Key takeaway:** Unlike overflow: hidden, clip-path can create non-rectangular shapes and can itself be animated for interesting reveal effects.
