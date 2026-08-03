# Common Animation Performance Pitfalls

Animating properties like width, height, top, left, or margin forces the browser to recalculate layout on every frame, which can cause visible jank on lower-powered devices. Animating transform and opacity instead lets the browser handle the work on the compositor thread, skipping layout and paint entirely.

```css
/* Avoid animating this */
.slow { transition: left 0.3s; }

/* Prefer this */
.fast { transition: transform 0.3s; }
```

**Key takeaway:** If an animation feels janky, the first thing to check is whether it is animating a layout-triggering property instead of transform or opacity.
