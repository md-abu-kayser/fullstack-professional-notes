# Styling Forms and Inputs

Form elements ignore many CSS properties by default and vary visually across browsers, so consistent styling usually requires explicitly resetting appearance and rebuilding focus states. :focus-visible in particular helps show focus rings only for keyboard users, not mouse clicks.

```css
input {
  appearance: none;
  border: 1px solid #ccc;
  border-radius: 6px;
  padding: 8px 12px;
}
input:focus-visible { outline: 2px solid #2563eb; }
```

**Key takeaway:** Never remove focus outlines without replacing them with a visible alternative - it is one of the most common accessibility regressions in real projects.
