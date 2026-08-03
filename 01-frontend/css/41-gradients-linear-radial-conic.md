# Gradients: Linear, Radial, Conic

CSS gradients generate smooth color transitions without needing an image file. linear-gradient moves along a straight line at a chosen angle, radial-gradient radiates outward from a center point, and conic-gradient sweeps around a center point like a color wheel.

```css
.hero { background: linear-gradient(135deg, #2563eb, #7c3aed); }
.badge { background: radial-gradient(circle, #fff, #ddd); }
.wheel { background: conic-gradient(red, yellow, green, blue, red); }
```

**Key takeaway:** Gradients are just background-image values, so they can be layered with real images using multiple comma-separated backgrounds.
