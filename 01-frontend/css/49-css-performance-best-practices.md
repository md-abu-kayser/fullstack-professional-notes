# CSS Performance Best Practices

CSS rarely becomes a bottleneck on its own, but a few habits matter at scale: avoid deeply nested selectors that are expensive to match, prefer transform/opacity for animation, minimize the use of expensive properties like box-shadow and filter on frequently repainted elements, and keep unused CSS out of the critical path with code splitting or purging tools.

```css
/* Avoid: deep, over-specific selector chains */
body div.container ul li a.link { }
/* Prefer: flat, purposeful class names */
.nav-link { }
```

**Key takeaway:** For most real-world sites, CSS file size and unused rules hurt performance more than selector matching speed - purge before you optimize matching.
