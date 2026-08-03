# CSS Filters and Blend Modes

filter applies graphical effects like blur, brightness, or grayscale directly to an element and its children, commonly used for image treatments or hover effects. mix-blend-mode instead controls how an element's content blends with whatever is behind it, similar to blend modes in image editing software.

```css
.photo:hover { filter: grayscale(0%) brightness(1.1); }
.overlay-text { mix-blend-mode: difference; }
```

**Key takeaway:** filter effects like blur can be expensive to animate - test on lower-end devices before shipping.
