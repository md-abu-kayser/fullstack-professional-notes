# The calc Function and Dynamic Values

calc() lets you mix units in a single expression - something plain CSS values cannot do otherwise, like subtracting a fixed pixel value from a percentage-based width. It is evaluated by the browser at render time, so it also works with CSS variables.

```css
.sidebar-content { width: calc(100% - 250px); }
.spaced { margin-top: calc(var(--spacing-unit) * 2); }
```

**Key takeaway:** Always leave spaces around the operators inside calc() - calc(100%-20px) is invalid, calc(100% - 20px) is required.
