# CSS Reset vs Normalize

A reset (like Eric Meyer's classic reset) aggressively strips all default browser styling to a blank slate, requiring you to rebuild everything from scratch. Normalize.css instead preserves useful defaults while fixing inconsistencies across browsers. Most modern projects use a small custom reset targeting just the handful of properties that cause the most cross-browser pain.

```css
*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
```

**Key takeaway:** A full aggressive reset is less common today - most teams prefer a minimal, targeted reset plus border-box sizing.
