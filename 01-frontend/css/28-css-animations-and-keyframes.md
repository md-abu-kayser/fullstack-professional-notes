# CSS Animations and Keyframes

@keyframes define a named sequence of styles at different points (0% to 100%) of an animation timeline, which is then applied to an element via the animation property. Unlike transitions, keyframe animations do not need a trigger - they can run automatically, loop, and have multiple intermediate steps.

```css
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}
.toast { animation: fadeIn 0.3s ease-out; }
```

**Key takeaway:** Use transitions for simple two-state changes (hover, toggle) and keyframe animations when you need multiple steps or looping behavior.
